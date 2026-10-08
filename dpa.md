# Stitchback – Merge & Undo for Jira: Data Processing Agreement

**under Article 28 GDPR, based on the Standard Contractual Clauses of Commission Implementing Decision (EU) 2021/915**

Version 1.0 · DRAFT of 7 October 2026 · not yet in force

---

## Part 1: Incorporation and choices

1.1 **Scope.** This Data Processing Agreement (**DPA**) forms part of the End User Terms for *Stitchback – Merge & Undo for Jira* (the **Product**). It is the "DPA" referred to in Section 3.3 of the Bonterms Standard End User Agreement (Version 1.0), as modified by the Provider-Specific Terms. It applies to the extent that the Provider processes personal data on behalf of the Customer, and that Regulation (EU) 2016/679 (**GDPR**) applies to that processing. Sections 1.6 and 1.7 extend it to UK, Swiss and U.S. state privacy laws.

1.2 **Incorporation.** The **Standard Contractual Clauses between controllers and processors** set out in the Annex to Commission Implementing Decision (EU) 2021/915 of 4 June 2021 (the **Clauses**) are incorporated into this DPA by reference. The official text is available at <https://eur-lex.europa.eu/eli/dec_impl/2021/915/oj>.

- The **Customer** is the controller.
- The **Provider** is the processor.

1.3 **Choices made in the Clauses:**

| Clause | Choice |
|---|---|
| Clause 1(a) | OPTION 1 (Article 28(3) and (4) GDPR) applies |
| Clause 5 (docking clause) | does not apply |
| Clause 7.7(a) | **OPTION 2 (general written authorisation)**. The time period for informing the Customer of intended changes is **10 days** |
| Clauses 9.1 and 9.2 | OPTION 1 (GDPR) applies |
| Annexes I–IV | as set out in Part 2 below |

1.4 **Precedence.** In the event of a contradiction between the Clauses and any other part of the End User Terms, the Clauses prevail (Clause 4).

1.5 **Additional terms.** The following terms supplement the Clauses. They do not contradict the Clauses (Clause 2(b)).

- (a) **Documented instructions.** The End User Terms, this DPA and the Customer's use and configuration of the Product are the Customer's documented instructions. Starting a merge or an undo in the Product is an instruction to carry out that operation.
- (b) **Audits (Clause 7.6).** The Provider will first answer audit requests by providing written information and the documentation listed in Annex III. On-site audits require reasonable prior notice and must take place during normal business hours. They are limited to what is necessary, and the Customer bears its own costs. The Provider operates no premises or systems that hold Customer personal data (Annex II). Atlassian's audit reports for the Forge platform are made available by Atlassian.
- (c) **Deletion or return (Clause 10(d)).** The Customer instructs the Provider to delete each merge record automatically 90 days after its last activity (Annex II, item 7). This deletion applies throughout the processing, including during any notice, transitional or retrieval period under Section 11 of the Provider-Specific Terms. Personal data deleted in this way is no longer processed on behalf of the Customer. At the end of the processing, the Customer exercises its choice under Clause 10(d) as follows:
  - **Return:** a Jira administrator of the Customer exports all merge records then stored, in JSON format, with **"Export all app data (JSON)"** on the Product's administration page (Jira settings → Apps). This function remains available until the Product is uninstalled. The Provider makes it available and does not restrict it.
  - **Deletion:** a Jira administrator of the Customer deletes all merge records with **"Delete all app data"** on the same page, at any time. Merges in progress at that moment are listed and are deleted only on the administrator's explicit confirmation. The Customer then uninstalls the Product. Uninstallation causes deletion by the sub-processor in accordance with Atlassian's Forge hosted-storage data lifecycle (Annex II, item 7).
  - **Certificate:** on request, the Provider confirms in writing that it holds no copies of the personal data outside the Forge hosted storage, and that deletion within the Forge hosted storage is effected by the means described above.
- (d) **Liability.** Liability between the parties under this DPA is governed by Section 8 of the Provider-Specific Terms. Nothing in this DPA limits the rights of data subjects, including under Article 82 GDPR.
- (e) **Governing law and courts.** These follow the End User Terms.

1.6 **UK and Switzerland.** This DPA also applies where the UK GDPR or the Swiss Federal Act on Data Protection (**FADP**) applies to the processing. In that case:

- references to the GDPR include the UK GDPR and the FADP, and references to Member States include the UK and Switzerland;
- the competent supervisory authority is the UK Information Commissioner or the Swiss Federal Data Protection and Information Commissioner (FDPIC);
- the general authorisation of sub-processors under Clause 7.7 is also the prior authorisation under Article 9(3) FADP;
- transfers to Atlassian are covered by the UK Addendum and the Swiss amendments in Sections 1.6(c) and (d) of Atlassian's Forge Data Processing Addendum.

1.7 **U.S. state privacy laws.** Where the California Consumer Privacy Act (CCPA) or another U.S. state privacy law applies to Customer personal data, the Provider acts as the Customer's service provider or processor, for the business purpose in Annex II, item 5. The Provider:

- does not sell or share the personal data;
- does not retain, use or disclose it for any other purpose, for any other commercial purpose, or outside the direct business relationship with the Customer;
- does not combine it with personal information from other sources, except as permitted by law;
- complies with the applicable obligations of these laws and provides the same level of privacy protection;
- notifies the Customer if it can no longer meet these obligations.

The Customer may take reasonable and appropriate steps to ensure such use, and to stop and remediate unauthorised use (Clause 7.6 and Section 1.5(b)). The Provider assists with consumer requests as set out in Annex III, item 10.

---

## Part 2: Annexes

### ANNEX I: List of parties

**Controller(s):**

- **Name, address:** the Customer, as identified in its Order on the Atlassian Marketplace.
- **Contact person:** the technical contact named in the Order.
- **Activities relevant to the data transferred under these Clauses:** use of the Product in the Customer's Jira Cloud site.
- **Signature and accession date:** the Customer accedes to this DPA electronically on its first Order for the Product, including any Free Use (Article 28(9) GDPR).

**Processor(s):**

- **Name:** Tom Gebauer (sole trader)
- **Address:** Marburger Tor 18, 57072 Siegen, Germany
- **Contact person:** Tom Gebauer, tom@alpscreen.de
- **Activities relevant to the data transferred under these Clauses:** provision of the Product as a Forge app running on Atlassian's cloud platform.
- **Signature and accession date:** by publishing the Product with these End User Terms.

### ANNEX II: Description of the processing

**1. Categories of data subjects whose personal data is processed**

- (a) users of the Customer's Jira site who use the Product (agents, team members);
- (b) authors of comments, attachments and issues that are merged;
- (c) requesters, reporters, watchers and request participants of merged issues, including customers of the Customer in Jira Service Management;
- (d) persons who are named in issue summaries, comments or attachments.

**2. Categories of personal data processed**

- (a) **Stored by the Product** in Forge hosted storage (merge records):
  - account ID of the user who starts a merge and of the user who undoes it;
  - account ID of a requester who is added as watcher or participant;
  - issue keys and issue status;
  - IDs of comments, attachments and links, and of the copies created;
  - sizes of attachments;
  - link types and linked issue keys;
  - role or group restrictions of copied comments;
  - timestamps and the status of each step.
- (b) **Processed transiently only** while a preview, merge or undo is running, and not stored by the Product: display names, issue summaries, file names, the content of comments and attachments, watchers, request participants and the requester's organisations, as read from and written to Jira.
- (c) **App log entries** (only if the Customer has not disabled log sharing): counts, merge IDs, issue keys, item IDs and error messages returned by Jira.

**3. Sensitive data processed (if applicable) and restrictions or safeguards applied**

The Product is not designed for sensitive data. Under Section 7.2 of the Standard Agreement, the Customer does not submit special categories of data (Article 9 GDPR). If such data is contained in issues anyway, it is processed only transiently, as described in item 2(b), with the measures in Annex III.

**4. Nature of the processing**

- reading the source and target issue through the Jira REST APIs with the acting user's permissions;
- copying comments and attachments;
- creating links, watchers and participants;
- writing audit notes;
- transitioning the source issue;
- storing and reading a merge record;
- on undo, removing what the merge created.

**5. Purpose(s) for which the personal data is processed on behalf of the controller**

To merge Jira issues and to undo merges, as requested by the Customer's users, and to find and fix errors and security issues in the Product.

**6. Duration of the processing**

For the term of the End User Terms, and in addition for the period described in item 7.

**7. Retention**

- **While installed:** each merge record is kept for 90 days after its last activity (start, progress, completion or undo), so that the merge can be undone during that time. A daily job of the Product then deletes the record and its index entries. A merge that is still in progress is not deleted by this job.
- **App logs:** available to the Provider for 30 days.
- **On request:** the Customer's Jira administrators can export and delete all merge records at any time on the Product's administration page (Part 1, 1.5(c)).
- **After uninstallation:** Atlassian retains the data according to its Forge hosted-storage data lifecycle. This includes access for 60 days after the end of the billing or trial period, unless the app is removed immediately. After that, the data is soft-deleted and then destroyed at the end of Atlassian's retention period.
- **During switching (EU Data Act):** the deletion described under "While installed" continues unchanged during any notice, transitional and retrieval period. The Customer can preserve the merge records as they stand at any moment by exporting them (Part 1, 1.5(c)).

**8. For processing by (sub-) processors, also specify subject matter, nature and duration of the processing**

Atlassian hosts the Product's functions and its storage for the duration set out in items 6 and 7 (see Annex IV).

### ANNEX III: Technical and organisational measures including technical and organisational measures to ensure the security of the data

1. **No own infrastructure.** The Product runs only on Atlassian's Forge platform. It declares no external network access (egress) and no remote back end. No personal data leaves Atlassian's platform through the Product.
2. **Least privilege.** The Product requests only the Jira and Jira Service Management scopes it needs. Every Jira request runs with the permissions of the acting user (`asUser`). The Product cannot access issues that the acting user cannot access.
3. **Data minimisation.**
   - The merge records hold only identifiers, timestamps and statuses. Display names, issue summaries, file names and the content of comments and attachments are not stored by the Product; they are read from Jira when needed.
   - Merge records are deleted automatically 90 days after their last activity.
   - The Product's code writes log entries only with counts and identifiers, never with names, summaries, file names or comment texts.
   - The Product does not delete the source issue or its content.
4. **Safe defaults and reversibility.**
   - Every merge shows a preview with warnings and needs explicit confirmation.
   - Comments copied into a service request are internal by default.
   - Undo removes what a merge created.
   - Interrupted merges are reconciled with Jira before they continue.
5. **Safety switch.** The Provider can stop all merges and undo operations immediately, for all installations. Nothing in Jira is changed while the switch is on.
6. **Platform security.** Atlassian provides encryption in transit and at rest, isolation between installations, and data residency for Forge hosted storage, as described in Atlassian's Forge documentation and Trust Center.
7. **Developer account security.** Access to the Provider's Atlassian developer account and API tokens is restricted to the Provider. The account is protected with two-factor authentication, and tokens are stored in the operating system's keychain.
8. **Vulnerability handling.** The Provider follows Atlassian's Security Bug Fix Policy for Marketplace apps (critical vulnerabilities within 10 days). It reports security incidents to Atlassian within 48 hours.
9. **Breach notification (Clause 9).** The Provider notifies the Customer of a personal data breach without undue delay. Where feasible, it does so within 48 hours of becoming aware of the breach, to the Customer's technical contact.
10. **Assistance with data subject requests (Clause 8).** The Customer's Jira administrators can export all merge records as JSON and delete them on the Product's administration page. The Product checks on every request that the user is a Jira administrator. On request, the Provider explains how to locate and remove data.

### ANNEX IV: List of sub-processors

The controller has authorised the use of the following sub-processor:

| Name | Address | Contact person | Description of the processing | Location |
|---|---|---|---|---|
| **Atlassian Pty Ltd** (and its sub-processors as listed at <https://www.atlassian.com/legal/sub-processors>) | Sydney, Australia (registered address as stated in Atlassian's Forge Data Processing Addendum and Developer Terms) | Head of Privacy, dataprotection@atlassian.com | Hosting and execution of the Product's functions; Forge hosted storage of merge records; app logs | According to the data residency of the Customer's Atlassian site, where supported; otherwise as determined by Atlassian |

**Transfers to third countries (Clause 7.8).** Atlassian Pty Ltd is located in Australia, for which no adequacy decision exists. Transfers to it and its sub-processors are made under the Standard Contractual Clauses of Commission Implementing Decision (EU) 2021/914, Module Three (processor to processor), as incorporated in Section 1.6(a) of Atlassian's Forge Data Processing Addendum, together with the UK Addendum (Section 1.6(c)) and the Swiss amendments (Section 1.6(d)). Atlassian, Inc. (United States) is certified under the EU-U.S. Data Privacy Framework.
