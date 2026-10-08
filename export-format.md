# Stitchback – Merge & Undo for Jira: Export Format

**Online register of data structures and formats (Article 26(b) of Regulation (EU) 2023/2854)**

Format `stitchback-export/1` · Product version 3.7.0 · DRAFT of 4 October 2026

---

## 1. How to get the export

A Jira administrator opens the Product's administration page (Jira settings → Apps) and selects **"Export all app data (JSON)"**. The Product checks on every request that the user is a Jira administrator. The export contains **every** key that the Product stores for the installation. Nothing stored is left out.

Merge records are deleted automatically 90 days after their last activity (End User Terms, Section 10.4). An export contains the records stored at the time of the export.

## 2. Standards

- **JSON** as defined in RFC 8259, encoded in UTF-8.
- **Timestamps** are numbers: milliseconds since 1970-01-01T00:00:00Z (Unix epoch). The only exception is `exportedAt` in the header, which is an ISO 8601 string in UTC.
- **Identifiers** are the identifiers Jira uses in its public REST API (issue keys, comment, attachment and link IDs, transition and status IDs, Atlassian account IDs). They can be resolved with the Jira Cloud REST API v3.

## 3. Document structure

```json
{
  "app": "Stitchback – Merge & Undo for Jira",
  "format": "stitchback-export/1",
  "exportedAt": "2026-10-04T12:00:00.000Z",
  "retentionDays": 90,
  "items": [
    { "key": "merge:<merge ID>", "value": { } },
    { "key": "running:<issue key>", "value": { } },
    { "key": "last:<issue key>", "value": "<merge ID>" },
    { "key": "retention:cursor", "value": "<opaque>" }
  ]
}
```

| Field | Meaning |
|---|---|
| `app`, `format` | Product name and format version. A change that is not backwards compatible gets a new format version |
| `exportedAt` | Time of the export |
| `retentionDays` | Retention period applied by the installation |
| `items` | All stored entries as key–value pairs, in storage order |

## 4. Keys

| Key | Value |
|---|---|
| `merge:<merge ID>` | The **merge record** (Section 5) |
| `running:<issue key>` | Lock while a merge of this source issue is running: `{ "id": <merge ID>, "at": <timestamp> }` |
| `last:<issue key>` | ID of the most recent merge in which this issue was source or target |
| `retention:cursor` | Where the daily clean-up stopped. Internal position marker, no personal data |

## 5. Merge record

| Field | Content |
|---|---|
| `v` | Version of the record structure (currently `3`) |
| `id` | Merge ID |
| `source` | `key`, `isServiceRequest`, `statusBefore` (status of the source before the merge) |
| `target` | `key`, `isServiceRequest` |
| `by` | `accountId` of the user who started the merge |
| `status` | `running`, `done`, `failed`, `undoing` or `undone` |
| `startedAt`, `activeAt`, `finishedAt`, `undoneAt` | Timestamps (where reached). The last activity is the latest of these and of `undo.startedAt` |
| `counts` | Number of items per type in the merge |
| `decisions` | `requester` (`op`, `accountId`, `reason`): whether the requester of the source was added to the target · `close` (`transitionId`, `reason`): how the source was closed |
| `steps` | One entry per step (Section 6) |
| `next` | Index of the next step to run |
| `warnings` | Notes recorded while the merge runs, for example that a comment was deleted during the merge and not copied, or why a step stopped. They contain issue keys, item IDs, status or role names and error messages from Jira. The warnings of the preview, which name people and files, are shown on screen and not stored |
| `failedAt` | If the merge stopped: `op`, `index` and `error` (the error message) of the step that failed |
| `undo` | Present once undo has started: `tasks`, `next`, `inFlight`, `notes`, `byAccountId` (account ID of the user who undid the merge), `startedAt` |

## 6. Step

Each step has `state` (`pending`, `done`, `failed` or `skipped`) and the fields below that apply to its operation `op`:

| Field | Content |
|---|---|
| `op`, `phase` | Operation (`copyComment`, `copyAttachment`, `mentionAttachment`, `addLink`, `addParticipant`, `addWatcher`, `linkDuplicate`, `auditComment`, `closeSource`) and its phase |
| `issue` | Issue key the step acts on |
| `from` | ID of the original item in the source issue |
| `internal`, `visibility` | Whether the copied comment is internal; its role or group restriction |
| `attachmentId`, `size` | ID and size in bytes of the original attachment |
| `type`, `direction`, `otherKey`, `existingLinkIds` | Link type, direction, linked issue key, IDs of links that already existed |
| `accountId` | Account ID of the requester added as participant or watcher |
| `duplicateOf` | Target issue key for the duplicate link |
| `transitionId`, `toStatusId` | Jira transition and status used to close the source |

When a step has created something, `created` records the IDs of the created items (for example the new comment, attachment or link), so that undo can remove exactly those.

## 7. What is not in the export

The Product does not store display names, issue summaries, file names, comment or attachment content, or email addresses (Privacy Policy, Section A3). This content stays in the Customer's Jira site and can be exported there with Jira's own tools.
