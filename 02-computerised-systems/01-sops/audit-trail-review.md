---
title: Audit Trail Review
sidebar_label: Audit Trail Review SOP
sidebar_position: 3
slug: /computerised-systems/operations/sop-audit-trail-review
api_id: c705b399-19eb-447c-a5b2-9f3836ebe3c2
api_type: sop
api_label: 02-SOP-ATR
api_version: "1.0"
api_status: draft
---

# 02-SOP-ATR: Audit Trail Review

## 1. Purpose and scope {#purpose-scope}

Use this procedure to examine GMP audit trails with their records, identify unexplained events and document the decision. It applies to computerised systems supporting human finished pharmaceuticals in EU and US operations.

**Draft reference template:** Quality and the System Owner must confirm local applicability, review reports, staffing, retention and escalation before adoption. The workflow is a proposed project control. Site audit-trail capabilities and reviewer capacity have not been verified.

Review covers record changes, deletions, processing and approval events, plus system events that can affect record reliability. This procedure does not replace batch release, laboratory review, deviations or CSV.

## 2. References and terms

- European Commission, [EU GMP Annex 11, January 2011](https://health.ec.europa.eu/document/download/8d305550-dd22-4dad-8463-2ddb4a1345f1_en?filename=annex11_01-2011_en.pdf), sections 9, 12.4 and 13.
- FDA, [21 CFR Part 11](https://www.ecfr.gov/current/title-21/chapter-I/subchapter-A/part-11), sections 11.1 and 11.10(e), when applicable; [21 CFR 211.192 and 211.194(a)(8)](https://www.ecfr.gov/current/title-21/chapter-I/subchapter-C/part-211).
- FDA, [Data Integrity and Compliance With Drug CGMP: Questions and Answers, December 2018](https://www.fda.gov/media/119267/download), questions 7 and 8; non-binding guidance.

An **audit trail** records system actions with their attribution and time. A **record-linked review** accompanies review of a specific GMP record. A **system-level review** examines events spanning records, including security or configuration events. **Quality** means the accountable Quality Unit.

## 3. Responsibilities {#responsibilities}

| Role | Responsibility |
| --- | --- |
| Data Owner | Identify critical records, metadata, lifecycle events and retention. |
| System Owner | Provide reliable reports, event descriptions, configuration evidence and system-level review coverage. |
| Trained record reviewer | Review the audit trail with its source record; document findings and unresolved questions. |
| IT administrator | Retrieve protected evidence and investigate technical faults without deciding GMP acceptability. |
| Quality | Approve review strategy, investigate data concerns and decide whether affected GMP decisions may proceed. |

Use a reviewer independent of the activity being reviewed. Assign trained deputies. IT assistance does not replace the record reviewer's judgement or Quality oversight.

## 4. Define review coverage {#review-coverage}

1. Before GMP use, the Data Owner and System Owner must prepare a Quality-approved review plan for each system.
2. List record types, critical fields, event sources, report versions, time zones, reviewer roles and review triggers.
3. Link record-level review to the review and approval of the associated GMP data. Complete review before batch release or the relevant quality decision.
4. For events without a prescribed record-review frequency, define the interval from data criticality, controls and potential product impact. Record the rationale and next due date.
5. Include relevant deletion, reprocessing, failed acquisition, date/time, role, audit configuration and administrator events. Explain which events are excluded and why they cannot affect the assessed records.
6. Validate any report, filter or automated exception rule used to select review evidence through CSV. Demonstrate that relevant events are retained and detectable.
7. Reassess coverage after changes to records, interfaces, reporting, permissions or audit configuration. Do not reduce review scope merely to clear a backlog.

## 5. Obtain and confirm evidence {#obtain-evidence}

1. The reviewer must identify the batch, sample, record version and review period before generating the report.
2. Retrieve the original record, relevant metadata, audit trail and linked change or deviation records using authorised read-only access.
3. Record the system, report version, filters, export time, time zone and inclusive period. Confirm identifiers match the source records.
4. Check pagination, truncation, retention limits and linked systems. Confirm that the period follows the previous completed review without an unexplained gap.
5. If the report contains no events, verify the search range and logging status. A blank report is not proof that no changes occurred.
6. If evidence is incomplete or the audit trail was disabled, hold the affected decision. Preserve available evidence and notify Quality and the System Owner immediately.
7. Do not recreate missing audit events or treat a user's recollection as equivalent to the original evidence.

## 6. Examine events and make decisions {#examine-events}

1. Review the trail in the context of the full record and approved process. Compare identity, timing, sequence and stated reason with the actual activity.
2. Check changed values against original values and authorised instructions. Confirm that changes did not obscure earlier information.
3. Examine repeats, reprocessing, aborted runs and deleted or excluded data. Link each relevant event to its documented explanation and investigation where required.
4. Compare changes after review or approval with change authority and the resulting record version. Reopen affected reviews when the decision basis changed.
5. For administrator or security events, determine which records and periods could be affected. Request technical interpretation from the System Owner when event meaning is unclear.
6. Record explained events with the supporting record reference. Record an event as unresolved when evidence does not support its purpose or acceptability.
7. Do not treat an available comment field, successful login or matching final result as proof that an event was authorised.

## 7. Escalate concerns and degraded conditions {#escalate-concerns}

| Condition | Required action |
| --- | --- |
| Unexplained deletion, manipulation or unauthorised change | Reviewer must preserve evidence and notify Quality immediately. Hold affected records and related GMP decisions pending assessment. |
| Possible impact on released product | Quality must initiate the deviation and quality-defect assessment. Identify other batches, products and periods that may share the failure. |
| Missing event meaning or conflicting explanation | Keep the question open. Obtain independent technical evidence and documented Quality disposition. |
| Reviewer absent or workload exceeds capacity | System Owner must assign a trained deputy or escalate resourcing to Quality. Keep release-dependent decisions on hold until required review is complete. |
| System or report unavailable | Preserve available source records. Use only a verified alternative that preserves review coverage, approved by Quality before relying on it. Otherwise maintain the hold. |
| Urgent production or release request | Apply the same evidence and approval criteria. Escalate priority; do not replace review with a promise of later review. |

Quality must define the affected population and investigation route under the deviation procedure. Keep original files protected. Corrections, report changes and restored functions remain subject to change control and CSV.

## 8. Verify completion and retain evidence {#verify-completion}

1. The reviewer must record completed scope, findings, supporting references, unresolved items and the conclusion with identity and date.
2. Verify that each relevant event has an explanation or linked investigation. Confirm that review gaps are reconciled and required Quality decisions are recorded.
3. If the closure check fails, return the review to open status. Maintain the affected decision hold and assign the missing action.
4. Quality must authorise removal of a GMP hold through the governing procedure. Audit review completion does not itself release a batch.
5. Retain the review evidence and audit trail with retrievable links to the source records. Apply the approved retention schedule, including applicable subject-record retention requirements.
6. If exports cannot preserve dynamic context, retain access to the source system or a validated equivalent. A screenshot alone is not sufficient when event details remain hidden.

## 9. Trends and practical check {#trends-check}

At the approved review interval, the System Owner must report overdue reviews, missing trails, unexplained events and recurring control failures to Quality. Include completed reviews as the denominator. Quality must assign investigation, CAPA or review-plan changes according to risk and recurrence.

For retrospective inspection or Quality review, retrieve a source record and demonstrate the full chain from report selection to event disposition and approval. If that chain cannot be reconstructed, open a deviation and assess other reviews using the same method.

**Completion check:** correct record and period; complete report; event context understood; unexplained events escalated; holds controlled; conclusion signed; evidence retrievable.
