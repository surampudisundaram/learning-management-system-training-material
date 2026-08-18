<!--
import: https://raw.githubusercontent.com/LiaPlayground/SCORM-Progress/main/README.md
-->

# GDPR Audit Checklist — Full LiaScript Lesson

This lesson converts `gdpr_audit_checklist.md` into a sectioned LiaScript course with:

- graded quiz items,
- hint and solution feedback,
- partial-solution display for multi-select questions,
- and a SCORM-ready progress gauge.

@score(GDPR Audit Score)

## How scoring works

- Each question includes a `data-score` value.
- Hints are shown with `[[?]]` blocks.
- Explanations under `**************************` act as solution feedback.
- When exported as SCORM, the score gauge reflects progress across the course.

## Evidence checklist summary

| Domain | Typical evidence |
| :--- | :--- |
| Data inventory | ROPA, DFDs, flow traces |
| Lawful basis | Lawful Basis Matrix, LIAs, consent logs |
| Data rights | DSAR SOP, identity checks, deletion evidence |
| Security | ACL reviews, pen tests, vuln scans, training logs |
| Incident response | Response plan, tabletop tests |
| Vendors | Due diligence, processor reviews, DPAs |
| SBOM | Generation logs, signatures, scans, VEX |
| Mapping | Component-to-activity matrix, risk flags |

---

## Section 1 — Audit workflow and data inventory

The audit starts by verifying the organization’s inventory of data processing activities and data flows.

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 1. What is the main purpose of the audit?
[( )] To verify policy wording only
[(X)] To verify operational evidence and how controls work in practice
[( )] To replace the legal review process

[[?]] Think about the difference between documentation and evidence that a control actually works.
**************************
**Feedback:** Correct — the audit checks operational evidence, not just policy text.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 2. Which phase comes first?
[( )] Security and Vendor Assurance
[(X)] Scoping and Data Inventory Verification
[( )] DSAR Stress Test

[[?]] The process begins by understanding what data exists and where it flows.
**************************
**Feedback:** Correct — inventory verification comes first.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 3. Which items should a ROPA explicitly list?
[[X]] Categories of data subjects
[[X]] Categories of personal data
[[X]] Recipients / third parties
[[ ]] Employee vacation preferences

[[?]] A ROPA should describe who is affected, what is processed, and who receives the data.
**************************
**Feedback:** Correct — those three categories are required for accountability.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 4. What gap does “shadow IT” usually indicate?
[( )] A fully approved and documented system
[(X)] An unrecorded data flow or tool outside the central inventory
[( )] A completed risk acceptance

[[?]] Shadow IT is a process or tool that exists in practice but not in the official inventory.
**************************
**Feedback:** Correct — unrecorded processing is a common audit gap.
**************************

---

## Section 2 — Lawful basis and consent

This section checks whether each processing activity has a legal justification and whether consent is recorded correctly.

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 5. Consent must be...
[(X)] Easy to withdraw as it was to give
[( )] Impossible to revoke once granted
[( )] Hidden in a separate policy page

[[?]] Think about how users should be able to change their minds.
**************************
**Feedback:** Correct — withdrawal must be as easy as giving consent.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 6. What must consent logs show?
[[X]] Timestamp
[[X]] IP address
[[X]] Exact wording agreed to
[[X]] Consent status
[[ ]] Favorite browser theme

[[?]] A consent record needs enough detail to reconstruct the event later.
**************************
**Feedback:** Correct — the logs must prove what was agreed to, when, and by whom.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 7. For legitimate-interest processing, which document should exist?
[(X)] Legitimate Interest Assessment
[( )] Employee handbook
[( )] Product roadmap

[[?]] This document records the balancing test between business need and individual rights.
**************************
**Feedback:** Correct — an LIA is expected for legitimate-interest processing.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 8. Which consent practice is unacceptable?
[( )] Explicit opt-in with a clear description
[(X)] Pre-checked boxes
[( )] A visible withdrawal mechanism

[[?]] Consent should be affirmative, not implied through preselection.
**************************
**Feedback:** Correct — pre-checked boxes are not valid consent practice.
**************************

---

## Section 3 — DSAR and data subject rights

This section tests whether the organization can handle access, deletion, and identity-verification requests in practice.

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 9. What is simulated during the DSAR stress test?
[( )] A vendor onboarding review
[(X)] A request for access or deletion
[( )] A quarterly access review

[[?]] DSAR exercises test whether the organization can retrieve or erase personal data on demand.
**************************
**Feedback:** Correct — the checklist uses a simulated request to test the process.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 10. What should identity verification protect against?
[(X)] Data leaks to an unauthorized requester
[( )] The need for any follow-up questions
[( )] The use of backup systems

[[?]] Verifying identity ensures the organization only discloses data to the right person.
**************************
**Feedback:** Correct — the control prevents accidental disclosure.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 11. Deletion evidence should prove deletion across...
[[X]] All storage locations
[[X]] Backups
[[X]] Third-party tools
[[ ]] Only the primary database

[[?]] Deletion has to propagate to every system that still holds the data.
**************************
**Feedback:** Correct — the proof must cover all relevant systems, including third parties and backups.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 12. Which document supports DSAR handling?
[(X)] A DSAR Standard Operating Procedure
[( )] A logo style guide
[( )] A product demo script

[[?]] The procedure should describe how requests are handled end to end.
**************************
**Feedback:** Correct — the audit expects a documented DSAR workflow.
**************************

---

## Section 4 — Security and vendor assurance

This section focuses on access control, security testing, incident response, and due diligence for processors.

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 13. Privileged access should be reviewed...
[( )] Daily
[(X)] Quarterly
[( )] Once every five years

[[?]] The checklist gives a recurring cadence rather than a one-time review.
**************************
**Feedback:** Correct — privileged access reviews are expected quarterly.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 14. Which evidence is requested for security testing?
[[X]] Penetration test reports from the last 12 months
[[X]] Recent vulnerability scan reports
[[X]] Proof that findings were remediated
[[ ]] Logo design files

[[?]] The evidence should show testing happened recently and issues were fixed.
**************************
**Feedback:** Correct — recent tests plus remediation evidence are required.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 15. Incident response evidence includes...
[[X]] Incident Response Plan
[[X]] Tabletop exercise records
[[ ]] Data retention waiver

[[?]] A plan alone is not enough; the organization should also show it has been exercised.
**************************
**Feedback:** Correct — the checklist looks for both the plan and practice.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 16. Vendor assurance focuses on...
[(X)] Security review records and due diligence for processors
[( )] Only vendor marketing materials
[( )] Personal opinions about the supplier

[[?]] The focus is documented due diligence for any processor handling personal data.
**************************
**Feedback:** Correct — vendor assurance is evidence-based.
**************************

---

## Section 5 — SBOM workflow

This section treats SBOM as a dynamic security control: generate, consume, and act.

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 17. SBOM stands for...
[(X)] Software Bill of Materials
[( )] Security Budget and Operations Manual
[( )] System Backup and Monitoring

[[?]] The acronym refers to a software inventory for the components you ship.
**************************
**Feedback:** Correct — SBOM means Software Bill of Materials.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 18. The SBOM workflow is described as...
[(X)] Generate-Consume-Act
[( )] Design-Build-Forget
[( )] Patch-Ship-Repeat

[[?]] The workflow mirrors the GDPR-style loop of inventory, verification, and action.
**************************
**Feedback:** Correct — generate, consume, then act.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 19. Which are NTIA minimum elements mentioned in the checklist?
[[X]] Supplier name
[[X]] Component name
[[X]] Version
[[X]] Unique identifiers
[[X]] Dependency relationship
[[X]] Author
[[X]] Timestamp
[[ ]] UI theme

[[?]] The checklist names seven fields that a baseline SBOM should include.
**************************
**Feedback:** Correct — these are the minimum elements called out in the workflow.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 20. SBOM generation should be triggered...
[(X)] Automatically after compilation/artifact creation
[( )] Only during annual audits
[( )] By a spreadsheet export

[[?]] The workflow pushes SBOM generation into CI/CD so it runs every build.
**************************
**Feedback:** Correct — SBOM generation should be automated in the pipeline.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 21. Why sign SBOMs with Sigstore/Cosign?
[[X]] To ensure integrity
[[X]] To support non-repudiation
[[X]] To help prevent tampering
[[ ]] To make builds slower on purpose

[[?]] Signing protects the SBOM after it is created.
**************************
**Feedback:** Correct — signing helps prove authenticity and detect tampering.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 22. What does VEX help with?
[[X]] Marking vulnerabilities as not affected
[[X]] Reducing noise in vulnerability management
[[ ]] Replacing source code reviews

[[?]] VEX explains whether a vulnerability actually affects the deployment.
**************************
**Feedback:** Correct — VEX helps separate relevant exposure from noise.
**************************

---

## Section 6 — SBOM ↔ ROPA mapping

This section links technical inventory to legal accountability by mapping software components to processing activities.

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 23. Which components are especially important to map to ROPA activities?
[[X]] Data-ingesting components
[[X]] Data-storing components
[[X]] Data-transmitting components
[[X]] Logging components
[[ ]] Wallpaper assets

[[?]] Focus on the components that actually touch personal data.
**************************
**Feedback:** Correct — those component types are most likely to affect processing risk.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 24. Which custom metadata tags are suggested for SBOM entries?
[[X]] handles_pii
[[X]] transmits_external
[[X]] stores_persistent
[[X]] logging_enabled

[[?]] These tags help classify how a component interacts with personal data.
**************************
**Feedback:** Correct — the tags are used to identify compliance-relevant behavior.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 25. Completeness in the mapping means...
[(X)] Every ROPA activity has at least one linked SBOM component
[( )] Every SBOM component has a celebrity nickname
[( )] Every risk is automatically resolved

[[?]] The mapping should cover all processing activities, not just the obvious ones.
**************************
**Feedback:** Correct — completeness means no ROPA activity is left unmapped.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 26. If a component is tagged `transmits_external` but the ROPA lists no recipients, what does that indicate?
[(X)] A compliance gap
[( )] A fully closed audit
[( )] No relationship between software and data processing

[[?]] External transfer in the software map should correspond to recipients in the legal map.
**************************
**Feedback:** Correct — that mismatch suggests undisclosed sharing or incomplete documentation.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 27. Which risk flag matches Log4j 2.14.1 in the example matrix?
[(X)] High
[( )] Low
[( )] None

[[?]] The example matrix marks the logging library as high risk because of the CVE.
**************************
**Feedback:** Correct — the example tags Log4j 2.14.1 as high risk.
**************************

<!-- data-score="1" data-hint-button="1" data-solution-button="true" -->
### 28. What does the mapping help reveal when a CVE is found in an SBOM component?
[[X]] Which ROPA activities are affected
[[X]] Which data subjects may be at risk
[[ ]] The office coffee budget

[[?]] A vulnerability in one component can affect multiple processing activities at once.
**************************
**Feedback:** Correct — the map shows which legal activities and data subjects are exposed.
**************************

---

## Section 7 — Remediation and reporting

If gaps are found, the audit must end with a structured remediation plan and ongoing monitoring.

<!-- data-score="2" data-hint-button="1" data-solution-button="true" -->
### 29. What should findings documentation record?
[[X]] Deficiencies
[[X]] Positive observations
[[ ]] Only the worst-case scenarios

[[?]] The checklist asks for balanced documentation, not just problems.
**************************
**Feedback:** Correct — auditors should record both weaknesses and positive evidence.
**************************

<!-- data-score="2" data-hint-button="1" data-solution-button="true" -->
### 30. For each gap, what should the action plan include?
[[X]] A specific recommendation
[[X]] An owner
[[X]] A target date for resolution
[[ ]] A random workaround

[[?]] A remediation plan should be specific enough to drive accountability.
**************************
**Feedback:** Correct — each gap needs a clear recommendation, owner, and due date.
**************************

<!-- data-score="2" data-hint-button="1" data-solution-button="true" -->
### 31. Which is an example of continuous monitoring mentioned in the checklist?
[(X)] Quarterly access reviews
[( )] One-time evidence capture only
[( )] No follow-up after the audit closes

[[?]] Monitoring keeps controls effective after the audit is over.
**************************
**Feedback:** Correct — recurring checks are part of the post-audit control model.
**************************

<!-- data-score="2" data-hint-button="1" data-solution-button="true" -->
### 32. A good risk rating should be based on...
[(X)] The potential impact on data subjects
[( )] How long the report is
[( )] Which spreadsheet format was used

[[?]] The checklist explicitly ties risk rating to the effect on individuals.
**************************
**Feedback:** Correct — risk should be rated by impact on data subjects.
**************************

---

## Wrap-up

You now have a full LiaScript lesson covering:

- the GDPR audit workflow,
- lawful basis and consent,
- DSAR handling,
- security and vendor assurance,
- SBOM generation and consumption,
- SBOM ↔ ROPA mapping,
- remediation and continuous monitoring.

### Optional next upgrades

1. Add an instructor-only answer key section.
2. Split the lesson into separate chapter files.
3. Add a SCORM mastery threshold when exporting.
4. Add more scenario-based questions using the same scoring pattern.
