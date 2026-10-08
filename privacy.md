# Stitchback – Merge & Undo for Jira: Privacy Policy

Version 1.0 · DRAFT of 7 October 2026 · not yet in force

This policy explains which personal data the app *Stitchback – Merge & Undo for Jira* (the **app**) processes, where, for how long, and who is responsible. It covers two situations:

- **Part A** covers data inside your Jira site. Here **you, the customer, are the controller** and I process data on your behalf.
- **Part B** covers data I process for my own purposes, such as support emails and licence records. Here **I am the controller**.

**Who I am.** Tom Gebauer, Marburger Tor 18, 57072 Siegen, Germany · tom@alpscreen.de · Legal notice (Impressum): <https://tomgebauerbuilds.substack.com/p/impressum>. I run the app as a sole trader. I am not required to appoint a data protection officer.

**Responsibility.** I, not Atlassian, am responsible for the processing of personal data by the app.

---

## Part A: Data inside your Jira site (I act on your behalf)

### A1. How the app works

The app is a Forge app. It runs entirely on Atlassian's cloud platform.

- **No servers of my own.** I operate no servers, databases or analytics tools of my own. The app sends no data outside Atlassian. Its manifest declares no external connections ("egress").
- **Your users' permissions.** Every access to Jira runs with the permissions of the user who uses the app. The app can only read and change what that user can read and change.
- **No personal data in the app's logs.** The app's code writes log entries only for its daily clean-up and for deletions on the administration page. These entries contain counts and identifiers (such as merge IDs and issue keys), never names, summaries, file names or comment texts.

### A2. What the app reads and changes in Jira

When a user previews or starts a merge, the app reads the source and target issues from Jira. This includes:

- summary, status, issue type, reporter or requester,
- comments, attachments, links, watchers,
- in Jira Service Management, request participants and the requester's organisations.

It then writes **in Jira**: copies of comments and attachments, links, watchers or participants, audit notes, and a status change of the source issue. The content of comments and attachments, the issue summary, file names and display names pass through the app's functions **only while a preview, merge or undo is running**. They are not stored by the app outside Jira. Where the app's screens or notes need a name, a summary or a file name, the app reads it from Jira at that moment.

### A3. What the app stores itself

The app keeps a **merge record** for each merge in Atlassian's Forge hosted storage (key–value store). The record is needed to resume an interrupted merge and to undo a merge. The storage keys are `merge:<merge ID>`, `running:<issue key>` and `last:<issue key>`, plus `retention:cursor` (where the daily clean-up stopped; no personal data). A merge record contains:

| Category | Content |
|---|---|
| Issues | issue keys of source and target; whether they are service requests; status of the source before the merge |
| Acting users | **account ID** of the user who started the merge and of the user who undid it |
| Time | timestamps of start, progress, completion and undo |
| Steps | IDs of the source comments, attachments and links and of the copies created; attachment sizes; link types and linked issue keys; role or group restrictions of copied comments; the **account ID of the requester** if the app added them as watcher or participant; the status of each step |
| Notes (`warnings`) | notes recorded while the merge runs, for example that a comment was deleted during the merge and not copied, or why a step stopped. They contain issue keys, item IDs, status or role names and error messages returned by Jira. The warnings of the preview, which name people and files, are only shown on screen and are not stored |

The app does **not** store display names, issue summaries, file names, the content of comments or attachments, email addresses, or any data from fields other than those listed above.

### A4. Where the data is stored

The data is stored in Atlassian's Forge hosted storage. It follows the **data residency** of your Atlassian site:

- If your site is pinned to a location, the data is stored there. Forge supports: Australia, Canada, the EU, Germany, India, Japan, Singapore, South Korea, Switzerland, the United Kingdom and the USA.
- If your site is not pinned, Atlassian decides in which of these locations the data is hosted, and may move it between them.
- Atlassian and its sub-processors may access the data from other countries, including Australia and the United States (see A7).

### A5. How long the data is kept

- **While the app is installed:** a merge record is kept for **90 days after its last activity** (start, progress, completion or undo). During that time the merge can be undone. A daily job then deletes the record together with its index entries. A merge that is still in progress is not deleted by this job; it is deleted 90 days after it has been completed or undone.
- **Deletion on request:** a Jira administrator can delete all merge records of the installation at any time with **"Delete all app data"** on the app's administration page (Jira settings → Apps). Merges in progress at that moment are listed and are only deleted when the administrator confirms this explicitly.
- **After you uninstall the app:** Atlassian keeps the data according to its Forge hosted-storage data lifecycle. You keep access for 60 days after the end of the billing or trial period, unless you remove the app immediately. After that, the data is soft-deleted and then destroyed at the end of Atlassian's retention period.
- **Reinstalling:** if you reinstall within 21 days of uninstallation and ask Atlassian, the new installation can be linked to the old data.
- **Source:** "Data lifecycle for Forge hosted storage", developer.atlassian.com, last updated 28 September 2026.

### A6. Who can access the data

- **Your users:** the status of the last merge of an issue is shown to users who open the app on that issue.
- **Your Jira administrators:** they can export all merge records of the installation as JSON with **"Export all app data (JSON)"** and delete them with **"Delete all app data"** on the app's administration page. The app checks on every request that the user is a Jira administrator.
- **Atlassian:** Atlassian hosts and processes the data as my sub-processor, under the Forge Data Processing Addendum. Atlassian may use its own sub-processors; see <https://www.atlassian.com/legal/sub-processors>.
- **Me:** I cannot view the content of the production storage of your installation in Atlassian's developer console. I can see **app logs** only if you have not disabled log sharing for the app in your site settings. These may contain error messages from failed requests to Jira, which can include issue keys and IDs.
- **Nobody else:** I do not sell or share the data.

### A7. Transfers outside the EU/EEA

- **Atlassian Pty Ltd** (Australia) is my sub-processor. It uses sub-processors in other countries, including the United States. There is no EU adequacy decision for Australia. My transfers to Atlassian are covered by the EU Standard Contractual Clauses (Decision (EU) 2021/914, Module Three: processor to processor), as incorporated in Section 1.6 of Atlassian's Forge Data Processing Addendum. For UK and Swiss data, the same section adds the UK Addendum and the Swiss amendments.
- **Atlassian, Inc.** (United States) is certified under the EU-U.S. Data Privacy Framework, its UK Extension and the Swiss-U.S. Data Privacy Framework.
- **Copy:** the Forge Data Processing Addendum is available at <https://developer.atlassian.com/platform/forge/about-the-forge-data-processing-addendum/>.
- **Government access:** if an authority demands your data from Atlassian, Atlassian will attempt to redirect the demand to me; if it is compelled to disclose, it gives me reasonable notice where the law allows (Forge Data Processing Addendum, Section 1.14). I hold no copies of your data. I will redirect such a demand to you and inform you, where the law allows.

### A8. Your rights and the rights of your users

You are the controller for the data in Part A. Requests from data subjects (for example your agents or your customers) should be addressed to you. I will help you answer them as set out in the Data Processing Agreement. The app stores only identifiers, timestamps and statuses. Your administrators can export them with "Export all app data (JSON)" and delete them with "Delete all app data" on the app's administration page. Everything else is in Jira and can be handled there.

### A9. Data Processing Agreement

The Data Processing Agreement under Article 28 GDPR is available at <https://tomgebauerservices.github.io/stitchback-legal/dpa>. It is part of the End User Terms.

---

## Part B: Data I process for my own purposes (I am the controller)

### B1. Support requests

**What:** if you write to me, I process your name, email address, company and the content of your message.

**Why:** to answer your request and to provide support under the End User Terms.

**Legal basis:** Art. 6(1)(b) GDPR where your request concerns a contract with me; otherwise Art. 6(1)(f) GDPR. My legitimate interest is to answer enquiries about the app.

**Do you have to provide the data?** No. But without an email address I cannot answer you.

**Recipient:** my email is hosted by Google Cloud EMEA Limited (Ireland) as my processor (Google Workspace). Google may transfer data to the United States. These transfers are covered by the EU-U.S. Data Privacy Framework, under which Google LLC is certified. Where Google transfers data to other countries without an adequacy decision, Standard Contractual Clauses apply.

**Retention:** I keep support emails as long as needed to handle the matter. Where an email is a business letter or an accounting record, I keep it for the statutory period under § 147 of the German Fiscal Code: 6 years for business letters, 8 years for accounting vouchers, 10 years for books and records, each from the end of the calendar year.

### B2. Licence and billing records from Atlassian

**What:** when you install, evaluate or buy the app, Atlassian provides me with licence records. These include your site, company, country, licence type and dates, and the names and email addresses of the technical and billing contacts.

**Source:** Atlassian Pty Ltd, from the Marketplace licence records.

**Why:** licence management, billing questions, support, and legally required records. Atlassian invoices you and collects payment as my commercial agent. Atlassian is responsible for its own processing of your payment data.

**Legal basis:**

- Art. 6(1)(b) GDPR: managing your licence and providing support;
- Art. 6(1)(c) GDPR: keeping records required by German tax law (§ 147 Fiscal Code, § 14b VAT Act);
- Art. 6(1)(f) GDPR: answering billing questions and defending legal claims. That is my legitimate interest.

**Retention:** as for B1.

### B3. App logs and platform metrics

**What:** Atlassian's developer console shows me aggregated platform metrics, such as installations, function calls and error rates. I do not use them to identify anyone. App logs are covered in Part A (A6): I use them only on your behalf, to keep the app working for you.

**Why:** to keep the app working, find errors and fix security issues.

**Legal basis:** Art. 6(1)(f) GDPR (legitimate interest in a secure and working app).

**Retention:** Atlassian shows me app logs for 30 days. Metrics are kept according to Atlassian's retention periods. I do not export either.

### B4. Marketplace listing

The Atlassian Marketplace listing is operated by Atlassian. For visits to it, Atlassian's privacy policy applies: <https://www.atlassian.com/legal/privacy-policy>.

### B5. Your rights

> **Your right to object (Art. 21 GDPR).** Where I process your data on the basis of legitimate interests (Art. 6(1)(f) GDPR), you can object at any time, on grounds relating to your particular situation. I will then stop, unless I can show compelling legitimate grounds that override your interests, or the processing is needed for legal claims. Write to tom@alpscreen.de.

You also have the right to:

- **access** your data (Art. 15 GDPR),
- **rectification** (Art. 16),
- **erasure** (Art. 17),
- **restriction** of processing (Art. 18), and
- **data portability** (Art. 20).

To exercise them, write to tom@alpscreen.de.

You can complain to any supervisory authority, in particular in the EU Member State where you live or work. The authority responsible for me is the Landesbeauftragte für Datenschutz und Informationsfreiheit Nordrhein-Westfalen, Postfach 20 04 44, 40102 Düsseldorf, Germany.

### B6. No automated decisions

I make no decisions based solely on automated processing, and I do no profiling.

---

## Changes

If the app starts to process data differently, I will update this policy. The version and date at the top show which version applies.
