# Stitchback – Merge & Undo for Jira: End User Terms

**Provider-Specific Terms to the Bonterms Standard End User Agreement (Version 1.0)**

Version 1.0 · DRAFT of 7 October 2026 · not yet in force

---

## How these terms are built

The agreement between you (the **Customer**) and the Provider for *Stitchback – Merge & Undo for Jira* (the **Product**) consists of:

1. the **Bonterms Standard End User Agreement (Version 1.0)** (the **Standard Agreement**), available at <https://www.atlassian.com/licensing/marketplace/end-user-agreement-v1>, and
2. these **Provider-Specific Terms**, including the Data Processing Agreement referred to in Section 10.

These Provider-Specific Terms modify the Standard Agreement under its Section 1.1. Under Section 1.4 of the Standard Agreement, they prevail over it. Where a section below says that it **replaces** a section of the Standard Agreement, the replaced section does not apply at all. Where it says that it **supplements** a section, both apply. Capitalised terms have the meaning given in the Standard Agreement unless defined here.

**Provider and notice address (Section 19.3(b) of the Standard Agreement):**
Tom Gebauer, Marburger Tor 18, 57072 Siegen, Germany · tom@alpscreen.de · Legal notice (Impressum): <https://tomgebauerbuilds.substack.com/p/impressum>

---

## 1. Relationship to Atlassian

1.1 **Atlassian is not a party.** Atlassian Pty Ltd and its affiliates (**Atlassian**) operate the Atlassian Marketplace and the Forge platform on which the Product runs. Atlassian is not a party to this Agreement (Section 19.4(b) of the Standard Agreement).

1.2 **Purchase, payment, refunds, taxes.** The Customer buys Subscriptions through the Atlassian Marketplace. Atlassian acts as the Provider's commercial agent. Ordering, invoicing, payment, refunds, taxes, evaluation (trial) licences, licence grace periods and licence tiers are governed by the Atlassian Marketplace Terms of Use and Atlassian's licensing policies. They are not governed by this Agreement. Section 10 (Fees) of the Standard Agreement applies accordingly.

1.3 **Jira and Forge.** Jira and Jira Service Management are Third-Party Platforms within the meaning of Section 8 of the Standard Agreement. The Customer's use of them is governed by its agreement with Atlassian. Atlassian hosts and runs the Product on the Forge platform as the Provider's sub-processor (Section 10.2). The Provider does not operate any servers of its own. The availability, performance, security and data residency of the Product depend on Jira and on the Forge platform. The Provider is not responsible for the failure of Jira or Jira Service Management, except as provided in Section 8 (Liability) of these terms. The Provider's responsibility for the Forge platform is governed by Section 8.

1.4 **Platform quotas and limits.** The Product is subject to the quotas, invocation limits and rate limits that Atlassian sets for Forge apps and for the Jira REST APIs. At the date of this version, these include a time limit per function call for user-interface functions. In practice:

- The Product runs a merge in **stages**. A large merge (many comments, attachments or links) may take several stages. During that time the merge screen must stay open, or the merge must be resumed.
- If Atlassian rate-limits or interrupts a call, a merge may pause or stop part-way. The Product records each completed step. An interrupted merge can be resumed or undone.
- Attachments above the size limit shown in the merge preview are **not copied**. A note on the target issue points to them instead.
- Atlassian may change these limits at any time. Changes may slow down or restrict the Product.

---

## 2. The Product and the Customer's responsibilities

2.1 **What the Product does.** The Product merges one Jira issue (the source) into another (the target):

- It copies comments, attachments and links of the source to the target.
- It optionally adds the requester of the source as a participant or watcher of the target.
- It links the source as a duplicate of the target and closes the source.
- It adds an audit note to both issues.

The Product does not delete the source issue or its content. **Undo** removes the copies that the merge created and reopens the source, as far as Jira allows. Undo is available for **90 days** after the last activity of a merge. After that the merge record is deleted (Section 10.4), and the merge can no longer be undone by the Product. Comments copied into a Jira Service Management request are posted as **internal** notes by default.

2.2 **Permissions of the acting user.** The Product acts in Jira **only with the permissions of the user who starts the merge**. The Customer is responsible for these permissions. The Customer is also responsible for the visibility settings of its projects and issues.

2.3 **Preview and confirmation.** Before every merge, the Product shows a preview with warnings. The Customer is responsible for reviewing the preview before confirming. The preview shows, for example, whether internal notes will become visible to a wider audience.

2.4 **Backups.** The Customer remains responsible for backing up its Jira data at intervals appropriate to its risk.

---

## 3. Free Use and evaluation licences

*(Replaces the definition "Trials and Betas" in Section 20 and Section 18 of the Standard Agreement.)*

3.1 **Free Use.** "Free Use" means any use of the Product without charge, including the free tier that the Provider may offer for small sites. Free Use is permitted for the Customer's business purposes for as long as the Provider offers it. The Provider may end or change a free tier for the future with at least 30 days' notice. Evaluation licences issued through the Atlassian Marketplace are governed by Atlassian's licensing policies (Section 1.2) and are also Free Use.

3.2 **Beta features.** The Provider may mark individual features as "beta". Beta features may be incomplete and may be withdrawn at any time.

3.3 **Liability.** Liability for Free Use and for beta features is governed exclusively by Section 8.

3.4 **Without an active licence.** If the Atlassian Marketplace reports the Customer's licence for the Product as not active, the Product does not start new merges. A merge that has already started is completed. Existing merges can still be undone for the period stated in Section 2. Viewing the status of past merges, the preview and the administration page with export and deletion (Section 11) remain available.

---

## 4. Warranties

*(Replaces Sections 6.2 and 6.3 of the Standard Agreement. Section 6.1 continues to apply.)*

4.1 **Statutory rights.** The Customer's statutory rights in respect of defects apply, subject to Section 8.

4.2 **Remedying defects.** The Customer should report defects to the Provider in reasonable detail. The Provider will use reasonable efforts to remedy reported defects within a reasonable time.

4.3 **No guarantee.** The Provider gives no guarantee (*Garantie*) and assumes no procurement risk. The only exception is a statement expressly designated as a "guarantee" in writing. Descriptions of the Product in the Listing and the Documentation are descriptions of features. They are not guarantees.

4.4 **Representations in the Standard Agreement.** The representations and warranties in Sections 6.1 and 19.13 of the Standard Agreement are contractual obligations. They are not guarantees (*Garantie*) within the meaning of Section 4.3.

---

## 5. Support; no SLA

*(Supplements Sections 5.1 and 5.2 of the Standard Agreement.)*

5.1 **Support.** The Provider provides support by email to the address stated above, in English or German, on German business days. Support is provided on a reasonable-efforts basis. **No response time, resolution time or availability is guaranteed.**

5.2 **No SLA.** No Service Level Agreement applies to the Product.

---

## 6. Safety switch and security suspension

*(Supplements Section 11 of the Standard Agreement.)*

6.1 **Safety switch.** The Product has a safety switch. When the switch is on, no new merges or undo operations can be started. Nothing is changed in Jira while the switch is on. Viewing the status of past merges remains possible.

6.2 **When the Provider may use it.** The Provider may switch on the safety switch, or otherwise suspend all or part of the Product, **without prior notice**. It may do so only to the extent necessary to remedy a security vulnerability or a serious defect, or to prevent loss of data or unauthorised access to data.

6.3 **Limits of a suspension.** The Provider will:

- limit the suspension to what is necessary,
- inform affected Customers without undue delay, through the Product or the Listing, and
- for paid Subscriptions, refund prepaid fees pro rata for any suspension that lasts more than 7 consecutive days. The refund is made through the Atlassian Marketplace where possible.

---

## 7. Third-party claims

*(Replaces Sections 15.1, 15.4 (as far as the Provider is the indemnifying party), 15.6 and 15.7, and the definition "Provider-Covered Claim" in Section 15.3, of the Standard Agreement.)*

7.1 **No indemnity by the Provider.** The Provider does not indemnify or defend the Customer against third-party claims.

7.2 **Provider's options.** If a third party asserts that the Product infringes its rights, the Provider may, at its option and expense, do one of the following:

- obtain the right for the Customer to continue using the Product,
- modify the Product so that it no longer infringes, without materially reducing its overall functionality, or
- terminate the affected Subscription and refund prepaid, unused fees.

7.3 **Statutory claims remain.** The Customer's statutory claims for defects in title remain unaffected, subject to Section 8.

7.4 **Customer indemnity.** Section 15.2 of the Standard Agreement (indemnification by the Customer) applies only where the Customer is responsible for the breach on which the claim is based.

---

## 8. Liability

*(Replaces Section 14 of the Standard Agreement in its entirety, and every other limitation or exclusion of liability in the Standard Agreement, including the liability limit in Section 18 and the "exclusive remedy" provisions in Sections 6.2(d) and 15.7.)*

8.1 **Unlimited liability.** The Provider is liable without limitation:

- (a) for damage caused intentionally or by gross negligence;
- (b) for injury to life, body or health;
- (c) under the German Product Liability Act (*Produkthaftungsgesetz*);
- (d) where the Provider has fraudulently concealed a defect, or has given a guarantee, to the extent of that guarantee; and
- (e) wherever liability cannot be limited under mandatory law.

8.2 **Slight negligence.** In all other cases, the Provider is liable for slight negligence only if it breaches a material contractual obligation.

- **Definition.** Material contractual obligations are obligations whose fulfilment is essential for the proper performance of this Agreement and on whose fulfilment the Customer regularly relies and may rely. Examples are the obligation to provide the Product substantially as described in the Documentation, and the obligation to process Customer Data only on the Customer's instructions.
- **Limit.** In such cases, the Provider's liability is limited to the damage that was foreseeable and typical for this type of contract at the time the Agreement was concluded.

8.3 **Amount.** In the cases of Section 8.2, the Provider's liability for each event giving rise to liability is further limited to the greater of:

- (i) **EUR 10,000**, and
- (ii) the fees paid by the Customer for the Product in the twelve (12) months preceding that event.

8.4 **Free Use.** Where Free Use (Section 3) is gratuitous within the meaning of Sections 521, 524, 599 and 600 of the German Civil Code, the Provider is liable only for intent and gross negligence, and for defects only where it fraudulently concealed them. Where those provisions do not apply to Free Use, Sections 8.2 and 8.3 apply. Section 8.1 remains unaffected in all cases.

8.5 **Loss of data.** Except in the cases of Section 8.1, the Provider's liability for loss or corruption of data is limited to the effort that would have been required to restore the data from backups made by the Customer at regular intervals appropriate to the risk.

8.6 **Initial defects.** Except in the cases of Section 8.1, the Provider's no-fault liability for defects that already existed when the Agreement was concluded (Section 536a(1), first alternative, German Civil Code) is excluded.

8.7 **Scope.** This Section 8:

- applies to all claims, whether in contract, tort or otherwise;
- also applies in favour of the Provider's employees, representatives and vicarious agents;
- does not alter the burden of proof; and
- does not limit any rights of data subjects under Article 82 GDPR.

8.8 **Limitation period.** Claims of the Customer for damages or reimbursement of expenses become time-barred one (1) year after the start of the statutory limitation period. This does not apply to claims under Section 8.1. It does not apply to claims for which the law prescribes a longer period that cannot be shortened by agreement.

---

## 9. Usage Data

*(Supplements Section 3.4 of the Standard Agreement.)*

The Product does not send any data to systems of the Provider. The only data the Provider receives about the Customer's use of the Product are the following, as provided by Atlassian:

- **Platform metrics:** for example, the number of installations and function calls, and error rates.
- **App logs:** only if the Customer has not disabled log sharing for the Product in its Atlassian site settings. The Provider uses app logs only on the Customer's behalf under the DPA (Section 10), to keep the Product working. They are not Usage Data.

Details are in the Privacy Policy (Section 10).

---

## 10. Data protection

*(Supplements Section 3.3 of the Standard Agreement.)*

10.1 **DPA.** To the extent the Provider processes personal data on behalf of the Customer, the **Data Processing Agreement** at <https://tomgebauerservices.github.io/stitchback-legal/dpa> applies. It is the "DPA" within the meaning of Section 3.3 of the Standard Agreement. It is based on the Standard Contractual Clauses of Commission Implementing Decision (EU) 2021/915.

10.2 **Sub-processors.** The Provider's sub-processor is Atlassian Pty Ltd, together with Atlassian's own sub-processors.

10.3 **Privacy Policy.** The Privacy Policy at <https://tomgebauerservices.github.io/stitchback-legal/privacy> describes what the Product stores, where and for how long.

10.4 **Deletion.** Section 12.4(b) of the Standard Agreement is replaced as follows: data stored by the Product is deleted in accordance with the DPA and the data lifecycle of Atlassian's Forge hosted storage. In particular:

- each merge record is deleted automatically 90 days after its last activity; a merge that is still in progress is not deleted automatically;
- the Customer's Jira administrators can delete all data stored by the Product at any time with "Delete all app data" on the Product's administration page.

This automatic deletion is a documented feature of the Product and part of the Customer's documented instructions under the DPA. It applies unchanged during any notice, transitional and retrieval period under Section 11. The Provider has no access to the Product's production storage and cannot suspend the automatic deletion for an individual Customer. These rules are described in the Privacy Policy.

---

## 11. Data export and switching (EU Data Act)

*(Supplements Section 12 of the Standard Agreement. Applies where Regulation (EU) 2023/2854 applies to the Customer.)*

11.1 **What can be exported.** The exportable data generated by the Customer's use of the Product are the **merge records** stored by the Product at the time of the export, together with their index entries: issue keys, issue status, step results, identifiers of the original and the copied items, timestamps and the account IDs of the acting users. The export contains **all** data stored by the Product for the installation. No stored data is exempted as internal to the Provider's service. The Provider's application logic and source code are not stored data and are not exportable data. The issues themselves remain in the Customer's Jira site and are not affected by switching.

11.2 **How to export; known restriction.** A Jira administrator of the Customer may export the merge records **at any time and without the Provider's involvement**, including after Free Use, in a structured, commonly used, machine-readable format (JSON), with "Export all app data (JSON)" on the Product's administration page (Jira settings → Apps). The data structures and the format are described in the online register at <https://tomgebauerservices.github.io/stitchback-legal/export-format> (format "stitchback-export/1"). **Known restriction:** merge records are deleted automatically 90 days after their last activity (Section 10.4). A merge record that has been deleted in this way is no longer part of the exportable data. A Customer who wishes to keep merge records for longer, or to keep the records as they stand at the time of a switching notice, exports them and keeps the export.

11.3 **Switching notice.** The Customer may request, with a notice period of no more than two (2) months, to:

- switch to another provider (giving the necessary details of that provider),
- port its exportable data to its own infrastructure, or
- have such data erased.

The Customer may give this notice at any time by email to the address stated above. The Provider will confirm receipt and will remind the Customer of Section 11.2, including the recommendation to export the merge records **immediately**. The Agreement ends, and the Provider will notify the Customer of its end, (a) when the switching process is complete, or (b) if the Customer chooses erasure, at the end of the notice period.

11.4 **Transitional period.** After the notice period, a transitional period of thirty (30) days follows. The Customer may extend it once, before or during that period, for a period it considers appropriate. During this period, the Agreement continues to apply and the Provider will:

- continue to provide the Product as described in the Documentation, including the export function and the automatic deletion under Section 10.4,
- give reasonable assistance and all relevant information for the Customer's exit strategy, to the Customer and to third parties authorised by it,
- inform the Customer of known risks to the continuity of the Product, in particular the automatic deletion under Section 10.4 and the platform limits under Section 1.4, and
- maintain a high level of security.

If 30 days are technically unfeasible, the Provider will inform the Customer within 14 working days after the switching request. It will give its reasons and propose an alternative period of no more than seven (7) months.

11.5 **Retrieval period.** After the transitional period, the Customer may retrieve its exportable data for at least thirty (30) days with "Export all app data (JSON)". The Provider will not restrict the export function during this period, and will maintain a high level of security of the data. The data available for retrieval are the merge records then stored by the Product (Section 11.1). Automatic deletion under Section 10.4 continues during this period. The Customer should retrieve its data **before uninstalling** the Product, because the export function is no longer available after uninstallation.

11.6 **Full erasure.** The Provider ensures full erasure of all exportable data after the retrieval period, as follows:

- at the end of the retrieval period at the latest, the Customer uninstalls the Product (or, if it has chosen erasure, deletes all data with "Delete all app data" and uninstalls the Product);
- uninstallation causes the erasure of all data stored by the Product in accordance with Atlassian's Forge hosted-storage data lifecycle, as described in the Privacy Policy. The parties agree on the end of that lifecycle as the date of full erasure;
- independently of this, every merge record not in progress is deleted 90 days after its last activity.

The Provider itself holds no copies of the exportable data outside the Forge hosted storage. This Section 11.6 sets out a contractual obligation under Article 25(2)(h) of Regulation (EU) 2023/2854. It is not a guarantee (*Garantie*) within the meaning of Sections 4.3 and 8.1(d).

11.7 **No switching fees.** The Provider charges no switching fees.

11.8 **Location and international access.** Information on the jurisdiction of the infrastructure on which the Product runs, and on the measures against unlawful international governmental access, is available at <https://tomgebauerservices.github.io/stitchback-legal/privacy>, Sections A4 and A7.

---

## 12. Changes to these terms

*(Supplements Sections 19.5 and 19.6 of the Standard Agreement.)*

12.1 **New versions.** The Provider may publish new versions of these Provider-Specific Terms. A new version applies to new Orders, and to renewals of a Subscription Term that begin after it has been published. A change within a running Subscription Term requires the Customer's consent.

12.2 **Version of the Standard Agreement.** The Standard Agreement applies in Version 1.0. It does not change automatically when Bonterms or Atlassian publish a new version.

---

## 13. Governing law and courts

*(Specifies the "Governing Law" and the "Courts" under Section 19.2(b) of the Standard Agreement.)*

13.1 **Governing law.** The Governing Law is the law of the Federal Republic of Germany. The UN Convention on Contracts for the International Sale of Goods (CISG) and German conflict-of-laws rules are excluded.

13.2 **Courts.** The Courts are the courts competent for Siegen, Germany, and they have exclusive jurisdiction for both parties. This applies where the Customer is a merchant (*Kaufmann*) or a legal entity under public law, where the Customer has no general place of jurisdiction in Germany, and in any other case to the extent legally permissible.

---

## 14. Severability

*(Replaces the second sentence of Section 19.7 of the Standard Agreement.)*

If any provision of this Agreement is or becomes invalid, the remaining provisions remain unaffected.

---

## 15. Language

This Agreement is concluded in English. Any translation is for information only and is not binding.
