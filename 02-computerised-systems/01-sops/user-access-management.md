---
title: User Access Management
sidebar_label: User Access Management SOP
sidebar_position: 2
slug: /computerised-systems/operations/sop-user-access-management
api_id: 5f51fe15-5236-4a9e-8ca9-521543971e36
api_type: sop
api_label: 02-SOP-ACCESS
api_version: "1.0"
api_status: draft
---

# 02-SOP-ACCESS: User Access Management

## 1. Purpose and scope {#purpose-scope}

Use this procedure to request, authorise, verify, review and remove access to GMP computerised systems supporting human finished pharmaceuticals. It covers employees, contractors, suppliers, privileged accounts and non-person accounts in EU and US operations.

**Draft reference template:** Before adoption, Quality and the System Owner must confirm applicability, named deputies, access rules and record locations. Site staffing, identity systems and technical capabilities have not been verified. The detailed workflow is a proposed project control; it is not a claim that each step is prescribed by law.

Electronic-signature configuration and system validation remain under the CSV procedure. Ordinary business systems without GMP impact are excluded.

## 2. References and terms

- European Commission, [EU GMP Annex 11, January 2011](https://health.ec.europa.eu/document/download/8d305550-dd22-4dad-8463-2ddb4a1345f1_en?filename=annex11_01-2011_en.pdf), sections 12 and 14.
- FDA, [21 CFR 211.68(b)](https://www.ecfr.gov/current/title-21/chapter-I/subchapter-C/part-211#p-211.68(b)) and [Part 11](https://www.ecfr.gov/current/title-21/chapter-I/subchapter-A/part-11), sections 11.1, 11.10(d), (g), (i), 11.100, 11.200 and 11.300, when applicable.
- FDA, [Data Integrity and Compliance With Drug CGMP: Questions and Answers, December 2018](https://www.fda.gov/media/119267/download), questions 4 and 5; non-binding guidance.

**Privileged access** permits security administration or changes beyond an ordinary operating role. A **non-person account** performs a defined automated service. **Quality** means the accountable Quality Unit.

## 3. Responsibilities {#responsibilities}

| Role | Responsibility |
| --- | --- |
| Process Owner | Confirm business need, training and incompatible duties. |
| System Owner | Maintain the approved access matrix and account inventory; coordinate verification and reviews. |
| Data Owner | Define retention and retrieval for access evidence supporting retained GMP records. |
| IT administrator | Implement authorised requests, protect credentials and preserve account history. |
| Quality | Approve GMP access-control exceptions and decide affected-record disposition. |
| Manager or contractor sponsor | Notify role changes, termination and end dates before access is no longer needed. |
| User | Use assigned access only; report suspected misuse immediately. |

Assign a trained deputy for each approval and verification role. No person may approve their own privileged access. An administrator must not independently verify their own privileged configuration.

## 4. Establish the access baseline {#access-baseline}

1. The System Owner must prepare an access matrix before account creation. Identify each role, permitted actions, prohibited combinations and approval authority.
2. Define separate operating and administration permissions. Restrict GMP record changes and approvals to named authorised people.
3. Record the owner, purpose and permitted interfaces of each non-person account. Prohibit interactive GMP work and electronic signatures through that account.
4. Define identity verification, authentication, inactivity, lockout, credential recovery and review settings through the approved system specification.
5. Identify Part 11 applicability through CSV. Before electronic-signature use, confirm identity verification, signature controls and applicable organisational certification to FDA. Check the CSV specification against applicable sections 11.200 and 11.300 for signature components, signing sessions, ownership and credential controls.
6. If technical limitations prevent the approved controls, open change control and a Quality exception assessment. Do not begin affected GMP use until Quality approves a demonstrably effective alternative or the limitation is corrected. An exception must not waive an applicable regulatory requirement.

## 5. Request and authorise access {#request-authorise}

1. The requester must open an access request before first use or a role change.
2. Record system, unique person identity, employer or sponsor, role, justification, start date, end date and required training evidence.
3. The Process Owner must compare requested duties against the access matrix. Identify conflicting permissions across systems where the same GMP decision is affected.
4. The System Owner must approve the technical role mapping. Route privileges outside the matrix to Quality before implementation.
5. If information conflicts or training is incomplete, return the request with the missing evidence identified. Do not copy another user's permissions as a substitute for assessment.
6. Use the named deputy when an approver is absent. Production pressure does not permit self-approval or shared credentials.

## 6. Provision and verify {#provision-verify}

1. IT must implement only the approved permissions on the authorised effective date.
2. Assign an individual account for attributable GMP actions. Do not reuse another person's identity or electronic signature.
3. Deliver initial credentials through the approved secure channel. Do not store passwords, tokens or recovery codes in the request record.
4. The verifier must compare effective permissions with the approved matrix. Check inherited groups, supplier access and prohibited actions without changing GMP production records.
5. Verify privileged access independently from the administrator who configured it. Preserve permission exports or equivalent evidence with date, system and verifier identity.
6. If permissions differ, disable the unintended permission before GMP use. Record correction and repeat the affected verification.
7. Notify the requester only after verification passes. Record activation time and user acknowledgement of account responsibility.

## 7. Changes, removal and credential incidents {#change-remove}

1. For a role change, remove obsolete permissions before enabling conflicting new duties. Use the request and verification steps above.
2. For a leaver, the sponsor must give IT the effective removal time. Disable access by that time across application, remote-access and linked identity services.
3. For suspected compromise or an unplanned termination, IT must restrict access immediately on verified notification. Notify the System Owner and Quality where GMP data may be affected.
4. Revoke active sessions and credentials where technically supported. Check connected local accounts that central identity removal does not disable.
5. Preserve account-to-person links, signatures, audit trails and historical records. Disabling access does not authorise record deletion.
6. Verify removal from effective-access evidence. If access remains possible, isolate the route and open an incident.
7. Before credential reset, verify identity using the approved method. Investigate suspected misuse through the deviation procedure; a password reset alone does not close the event.

## 8. Temporary and emergency access {#emergency-access}

1. For supplier or emergency work, the System Owner must record the incident, named user, permitted actions and expiry before activation.
2. Obtain approval from an authorised person other than the requester. Use the pre-approved emergency matrix and deputy arrangement when ordinary approval is unavailable.
3. If no authorised approver is available, stop the affected GMP activity or use the approved continuity procedure. Do not grant unapproved privileges.
4. IT must limit access to the approved duration and scope. Record the session and changes using approved monitoring that protects credentials.
5. At expiry, disable access and verify removal. The System Owner must review performed actions before closing the request.
6. Quality must assess unexpected GMP changes before affected records support a decision. Route lasting configuration changes through change control and CSV.

## 9. Review, records and closure {#review-records}

The System Owner must set an approved review frequency using privilege, data criticality, staff turnover and exposure. Also review after suspected misuse, organisational changes or control failure.

Compare the complete effective-account list with current personnel, sponsors, training, approved roles and end dates. Include dormant, local, privileged, supplier and non-person accounts. Do not rely only on the request list. Assign discrepancies to named owners with deadlines based on exposure. Remove unauthorised access immediately; assess historical activity with Quality.

Close each request only when approval, implementation and independent verification where required agree. Retain identity, permissions before and after, timestamps, approvals, expiry, verification, exceptions and linked deviations in the controlled access register. The Data Owner must apply the approved retention schedule while preserving historical attribution for retained GMP records.

Quality and the System Owner must review overdue removals, unauthorised access, failed verifications and repeat exceptions at the approved review interval. Assign systemic causes to CAPA; do not substitute training for an unresolved technical weakness.

**Closure check:** approved need; trained person; correct effective rights; prohibited rights absent; expiry active; verification recorded; exceptions dispositioned.
