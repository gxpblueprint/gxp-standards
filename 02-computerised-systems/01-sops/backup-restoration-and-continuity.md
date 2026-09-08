---
title: Backup, Restoration and Continuity
sidebar_label: Backup, Restoration and Continuity SOP
sidebar_position: 4
slug: /computerised-systems/operations/sop-backup-restoration-and-continuity
api_id: 1db67399-c7fd-4e18-8a58-6e07cfcc01ff
api_type: sop
api_label: 02-SOP-BACKUP
api_version: "1.0"
api_status: draft
---

# 02-SOP-BACKUP: Backup, Restoration and Continuity

## 1. Purpose and scope {#purpose-scope}

Use this procedure to protect GMP data, maintain controlled work during outages and restore computerised systems to GMP service. It applies to EU and US human finished-pharmaceutical operations, including outsourced and cloud services.

**Draft reference template:** Before adoption, Quality, the Process Owner and IT must approve system-specific recovery plans and demonstrate operational capability. Site infrastructure, suppliers, recovery times and manual capacity have not been verified. Detailed controls below are project design choices requiring adaptation.

This procedure covers backup monitoring, recovery testing, incident triage, continuity, restoration and reconciliation. Record retention and archiving remain subject to data-integrity and document-control procedures. A rotating backup is not a substitute for an archive.

## 2. References and definitions

- European Commission, [EU GMP Annex 11, January 2011](https://health.ec.europa.eu/document/download/8d305550-dd22-4dad-8463-2ddb4a1345f1_en?filename=annex11_01-2011_en.pdf), sections 7, 13, 16 and 17.
- FDA, [21 CFR 211.68(b)](https://www.ecfr.gov/current/title-21/chapter-I/subchapter-C/part-211#p-211.68(b)).
- FDA, [21 CFR Part 11](https://www.ecfr.gov/current/title-21/chapter-I/subchapter-A/part-11), sections 11.1 and 11.10(a)–(c), when applicable.

**Recovery point objective (RPO)** is the approved maximum tolerable interval of data loss. **Recovery time objective (RTO)** is the approved target interval to restore the defined service. Neither objective authorises destruction of required records or unsupported GMP decisions. **Quality** means the accountable Quality Unit.

## 3. Responsibilities {#responsibilities}

| Role | Responsibility |
| --- | --- |
| Process Owner | Define critical activities, interruption limits and acceptable continuity operations. |
| Data Owner | Identify complete record sets, dependencies and reconciliation criteria. |
| System Owner | Own recovery plans, supplier interfaces, test schedules and service status. |
| IT recovery lead | Monitor backups, contain technical incidents, restore systems and provide verification evidence. |
| Quality | Decide GMP impact, approve continuity conditions and authorise return to GMP service. |

Assign deputies and out-of-hours contacts before operation. IT declares technical readiness; Quality decides GMP acceptability. Follow the deviation procedure for investigation and CAPA, and change control and CSV for changed configurations or validation impact.

## 4. Establish and test the recovery plan {#recovery-plan}

1. The System Owner must document system boundaries, dependent infrastructure, interfaces, supplier contacts and recovery sequence before GMP use.
2. The Data Owner must inventory raw data, metadata, audit trails, configurations, signatures and required reader software. Include retained archives where recovery affects their retrieval. Include credentials or keys needed for recovery in controlled secure custody, separate from ordinary recovery records.
3. The Process Owner and Quality must approve RPO, RTO, maximum tolerable interruption and continuity limits using product, process and record risk.
4. IT must define backup scope, frequency, retention, protected locations, access, separation from live-system failure and evidence of completion. Explain how the design meets the approved objectives.
5. Specify monitoring frequency, alert thresholds, responders, acknowledgement limits and escalation before the next exposure can breach the RPO.
6. Define restore-test frequency from change rate, criticality and previous failures. Test complete representative records, dependencies and recovery duration through CSV before use and at the approved interval.
7. Challenge unavailable infrastructure, corrupted backups and unavailable supplier support. Record failed criteria and correct them before relying on the recovery arrangement. For changes affecting archive retrieval, test retained-record access through the data-integrity procedure.
8. Before relying on continuity arrangements, the Process Owner must lead a representative test with operators, Quality and IT.
9. Before testing, Quality and the Process Owner must approve activation-time, workload-capacity and maximum-duration acceptance criteria.
10. Test outage recognition, contact escalation, alternative-workflow activation, controlled manual work and reconciliation back to the restored system. Include representative records and interfaces.
11. Record actual activation time, sustainable workload, operating duration and reconciliation results against the approved criteria.
12. If any criterion fails, prohibit reliance on the affected alternative. Correct the failure and repeat affected tests before approval.

## 5. Run backups and respond to failures {#backup-monitoring}

1. IT must review scheduled backup results at the approved interval. Compare expected jobs and data scope with completed jobs; a missing job is a failure.
2. Record backup identity, system, time, data period, verification result and storage location reference. Protect the backup against unauthorised alteration and deletion.
3. On failure, investigate the cause and determine the last verified recoverable point. Do not treat rerun success as proof that the missed interval is covered.
4. Notify the System Owner and Quality when recovery objectives or GMP records may be affected. Record exposure, containment and the next decision time.
5. If protection cannot meet the approved limit, the Process Owner must stop dependent work or activate approved continuity conditions.
6. Escalate unacknowledged alerts to the named deputy or management contact. Retain failure and correction evidence; do not erase failed-job history.

## 6. Triage the incident and control continuity {#incident-continuity}

1. On an outage or suspected corruption, the user must stop affected transactions and notify the support contact and Process Owner immediately.
2. IT must open an incident record and preserve logs and the damaged state where safe. Contain suspected compromise before connecting restored services.
3. The System Owner must identify affected systems, last known good time, interrupted transactions and supplier dependencies. Record uncertainty explicitly.
4. Quality must assess affected data, batches and decisions through the deviation procedure. Place affected GMP decisions on hold where reliability is uncertain.
5. The Process Owner must activate only the approved alternative workflow. Record the start time, permitted activities, duration limit and responsible staff.
6. Use controlled forms with unique identifiers for manual work. Record activity contemporaneously, including operator, actual time, batch or sample, checks and approvals.
7. Track issued forms and transactions for later reconciliation. Do not backdate later system entries or perform operations whose required controls cannot be maintained manually.
8. If an approver or safe alternative is unavailable, stop the affected activity. Escalate urgency through named deputies; production pressure does not authorise an improvised GMP process.

## 7. Restore and verify the system {#restore-verify}

1. IT must propose the recovery point, backup identity, target environment and restoration sequence. Identify the potential data-loss interval before restoration.
2. Obtain System Owner authorisation for technical recovery. Obtain Quality agreement to the verification and reconciliation plan before GMP use.
3. Restore into an isolated environment where practical. Prevent interfaces, scheduled jobs or user sessions from creating unintended transactions during verification.
4. Verify backup integrity and restore the required data and configuration together. Preserve originals and record every recovery attempt and failure.
5. Check versions, security, time settings, audit trails, record readability, signatures and representative calculations against approved criteria. Confirm restored archives remain accessible with complete, accurate records.
6. Confirm interfaces and critical workflows through CSV-defined verification. Record actual elapsed recovery time and the restored data point against the approved objectives.
7. If verification fails, keep the service unavailable for GMP use. Investigate, select a justified alternative recovery approach and repeat affected checks under the recorded plan.

## 8. Reconcile and return to GMP service {#return-service}

1. The Data Owner must reconcile the interval from the restored point through final cutover. Include manual records, local instrument files and upstream and downstream systems.
2. Account for queued, failed, duplicated, partially processed and already acknowledged interface transactions. Decide which transactions to replay, cancel or enter through approved controls.
3. Preserve each original record and identify later transcription as a later entry. Verify critical transcription by a second person or validated electronic means.
4. Compare record counts, identifiers, values, approvals and transaction status against the reconciliation plan. Investigate unexplained differences; do not create data to fill an unsupported gap.
5. IT must confirm technical readiness and restored monitoring. The Process Owner must confirm process readiness and the end of manual operation.
6. Quality must review verification, reconciliation, unresolved incidents and product impact before authorising GMP service. Define any bounded restrictions, owners and expiry in the authorisation.
7. Do not release affected batches or records while their reliability remains unresolved. Use the governing batch or investigation procedure for disposition.
8. Record the cutover time and notify users of permitted work. Monitor the first resumed transactions and verify that interfaces do not duplicate or omit records.

## 9. Records, closure and trends {#records-trends}

The System Owner must retain the approved plan, backup logs, alerts, incident timeline, continuity records, restore results, reconciliation and return authorisation in the controlled recovery record. The Data Owner must assign retention that protects required GMP evidence and linked records.

Close recovery only after failed criteria are dispositioned, continuity records are reconciled and follow-up actions have accountable owners. Quality must approve the GMP closure decision; an open CAPA requires a linked owner and due date.

At the approved review interval, report scheduled and successful backups, failures, missed alerts, restore-test results, recovery-objective breaches and reconciliation defects. Quality and IT must assign recurring causes to the deviation/CAPA process and reassess recovery plans after material changes or incidents.
