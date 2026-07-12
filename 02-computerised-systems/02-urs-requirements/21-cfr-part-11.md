---
title: 21 CFR Part 11 URS Requirements
sidebar_label: 21 CFR Part 11
slug: /computerised-systems/urs-requirements/21-cfr-part-11
api_id: 019f4cbd-6593-728c-a7ce-28e675a1d5f2
api_type: collection
api_version: "1.0"
api_status: published
---

# 21 CFR Part 11 URS Requirements

Use this collection as a starting library when defining requirements for a computerized system that creates, modifies, maintains, archives, retrieves, transmits, or signs regulated electronic records.

> **Drafting rule:** Select each requirement only after assessing intended use, electronic-record scope, electronic-signature scope, applicable predicate rules, system architecture, supplier capabilities, and risk. This collection is not an exhaustive or universally applicable Part 11 checklist.

The requirements are mapped directly to current 21 CFR Part 11 references. The normalized statements and applicability guidance clarify where implementation details are examples rather than verbatim regulatory wording; implementation details such as RAID, role names, password values, and file formats are examples that require organization-specific justification.

Every requirement has its own permanent UUID. Human labels may evolve, but UUID identity must not change.

## Audit trail integrity, records, and protection

### URS-P11-001

**Detect altered audit trail entries**

> The system must be capable of detecting audit trail entries that have been altered since they were originally generated.

- **Permanent UUID:** `019f4cbc-ba4b-73ca-bef1-e538397cd123`
- **Applicability:** Include only when the selected system supports this detection. Otherwise assess alternative controls, supplier limitations, and residual risk.
- **21 CFR Part 11 reference:** § 11.10(a).

### URS-P11-002

**Restrict desktop administrative access**

> The system must restrict desktop administrative access to authorized administrator users.

- **Permanent UUID:** `019f4cbc-ba54-704c-aa23-c7b8e1c5693b`
- **Applicability:** Apply where a user-accessible desktop or operating-system layer exists. Define service, vendor, emergency, and break-glass access separately.
- **21 CFR Part 11 reference:** § 11.10(a); related access controls in §§ 11.10(d) and 11.10(g).

### URS-P11-003

**Export batch records**

> The system must be able to generate a batch record in PDF or CSV format.

- **Permanent UUID:** `019f4cbc-ba54-704c-aa23-cb1045628049`
- **Applicability:** Apply only where the system creates or maintains batch records. Confirm that exports preserve the complete record, context, metadata, and relationships.
- **21 CFR Part 11 reference:** § 11.10(b).

### URS-P11-004

**Export audit trails**

> The system must be able to generate audit trail exports in PDF or CSV format.

- **Permanent UUID:** `019f4cbc-ba54-704c-aa23-cdc1b45bdba0`
- **Applicability:** Verify that exports remain complete, readable, attributable, correctly ordered, and linked to affected records. PDF or CSV may require supporting metadata or a native export.
- **21 CFR Part 11 reference:** §§ 11.10(b) and 11.10(e).

### URS-P11-005

**Perform periodic backups**

> The system must provide a mechanism for periodic backups.

- **Permanent UUID:** `019f4cbc-ba54-704c-aa23-d209fed02461`
- **Applicability:** Define scope, frequency, retention, security, monitoring, restoration testing, and recovery objectives. A backup mechanism alone does not demonstrate recoverability.
- **21 CFR Part 11 reference:** § 11.10(c).

### URS-P11-006

**Use mirrored storage**

> Applicable PCs and servers must be configured with RAID 1 mirroring.

- **Permanent UUID:** `019f4cbc-ba54-704c-aa23-d4186b93af21`
- **Applicability:** Use only when RAID 1 is justified for the architecture. RAID is not a backup and may not apply to cloud, managed, virtualized, appliance, or supplier-hosted systems.
- **21 CFR Part 11 reference:** § 11.10(c).

### URS-P11-007

**Disable unused physical ports**

> Unused physical USB and Ethernet ports that are not necessary for system operation must be disabled or physically blocked.

- **Permanent UUID:** `019f4cbc-ba54-704c-aa23-d991bcc61f92`
- **Applicability:** Apply to interfaces within the organization's control after assessing maintenance, support, emergency recovery, and approved peripheral needs.
- **21 CFR Part 11 reference:** § 11.10(d).

### URS-P11-008

**Secure servers in lockable cabinets**

> Servers must be located in lockable cabinets.

- **Permanent UUID:** `019f4cbc-ba54-704c-aa23-de6b28ed80dd`
- **Applicability:** Apply to on-premises servers where cabinet locking is part of the physical-security design. Controlled data rooms, managed data centres, cloud services, and sealed appliances may use different controls.
- **21 CFR Part 11 reference:** § 11.10(d).

### URS-P11-009

**Record specified audit trail events**

> The system must generate time-stamped audit trails that record applicable user actions and events, including user login, user logout, parameter changes, and alarm acknowledgement.

- **Permanent UUID:** `019f4cbc-ba54-704c-aa23-e0baac93c0c4`
- **Applicability:** Define the event inventory from intended use and risk. Include events relevant to regulated records, security, record context, and regulated decisions.
- **21 CFR Part 11 reference:** § 11.10(e).

### URS-P11-010

**Display minimum audit trail details**

> The audit trail must identify the user who performed each applicable action or event, the date and time it occurred, and a description of the action or event.

- **Permanent UUID:** `019f4cbc-ba54-704c-aa23-e44932da80f0`
- **Applicability:** Add old value, new value, reason for change, record identifier, signature meaning, or other context where intended use and risk require it.
- **21 CFR Part 11 reference:** § 11.10(e).

### URS-P11-011

**Prevent audit trail overwriting**

> The system must ensure that new audit trail entries do not overwrite or modify existing entries.

- **Permanent UUID:** `019f4cbc-ba54-704c-aa23-e997c7395c22`
- **Applicability:** Include retention, archival, capacity, purge permissions, database administration, and supplier-support paths rather than testing only normal user functions.
- **21 CFR Part 11 reference:** § 11.10(e).

## Time controls

### URS-P11-012

**Synchronize system time**

> The system time must be synchronized with an approved authoritative time source, such as domain network time or an NTP server.

- **Permanent UUID:** `019f4cbc-ba54-704c-aa23-eed264b20295`
- **Applicability:** Define the authoritative source, permitted tolerance, monitoring, failure indication, time-zone handling, setting permissions, and recovery after disconnection.
- **21 CFR Part 11 reference:** § 11.10(e).

### URS-P11-013

**Display date and time format**

> The system must display date and time in the format DD/MMM/YYYY and HH:MM.

- **Permanent UUID:** `019f4cbc-ba54-704c-aa23-f3fbb2416a8d`
- **Applicability:** Treat the format as the book's example, not verbatim Part 11 text. Select an unambiguous approved format and define time zone, seconds, and export behavior where needed.
- **21 CFR Part 11 reference:** § 11.10(e).

### URS-P11-014

**Adjust for daylight saving time**

> The system must adjust for daylight saving time automatically.

- **Permanent UUID:** `019f4cbc-ba54-704c-aa23-f4cc1420018c`
- **Applicability:** Apply only where local time and daylight-saving rules are used. UTC systems or regions without seasonal changes require different requirements.
- **21 CFR Part 11 reference:** § 11.10(e).

## Identity, authentication, and passwords

### URS-P11-015

**Enforce unique usernames**

> The system must enforce unique usernames by preventing duplicate usernames from being created.

- **Permanent UUID:** `019f4cbc-ba54-704c-aa23-fa8d46edc7f7`
- **Applicability:** Define renamed users, reused identifiers, service accounts, federated identity, deleted accounts, and cross-site directories so historical attribution remains unambiguous.
- **21 CFR Part 11 reference:** §§ 11.10(d) and 11.10(g); see also § 11.300(a) for electronic signatures.

### URS-P11-016

**Authenticate with unique credentials**

> The system must require authentication with a unique username and password before allowing a user to log in.

- **Permanent UUID:** `019f4cbc-ba55-70fb-b757-df256eeca83f`
- **Applicability:** Federated identity, smart cards, passkeys, biometrics, or multifactor authentication require equivalent approved requirements that preserve individual attribution.
- **21 CFR Part 11 reference:** §§ 11.10(d) and 11.10(g).

### URS-P11-017

**Obscure password entry**

> The system must obscure passwords while they are being entered.

- **Permanent UUID:** `019f4cbc-ba55-70fb-b757-e0f59178e371`
- **Applicability:** Apply to interfaces accepting passwords. Do not expose passwords in logs, exports, or error messages; assess any temporary reveal control.
- **21 CFR Part 11 reference:** § 11.10(g).

### URS-P11-018

**Protect stored passwords**

> The system must store passwords in a non-human-readable form, such as a suitably protected one-way hash.

- **Permanent UUID:** `019f4cbc-ba55-70fb-b757-e6f3655a3116`
- **Applicability:** Confirm current approved hashing, salting, work factors, key or pepper protection, migration, backup exposure, and supplier controls.
- **21 CFR Part 11 reference:** § 11.10(g).

### URS-P11-019

**Enforce password complexity**

> The system must enforce passwords of at least eight characters containing uppercase letters, lowercase letters, numbers, and special characters.

- **Permanent UUID:** `019f4cbc-ba55-70fb-b757-eb38cc91a949`
- **Applicability:** Treat the values as an example, not verbatim Part 11 text. Select current organization-approved controls based on threat, system capability, identity-provider policy, and user burden.
- **21 CFR Part 11 reference:** § 11.10(g).

### URS-P11-020

**Allow password changes**

> The system must allow users to change their password securely.

- **Permanent UUID:** `019f4cbc-ba55-70fb-b757-ef14303acbd6`
- **Applicability:** Define current-password verification, identity-provider ownership, session handling, notification, audit logging, and centralized authentication behavior.
- **21 CFR Part 11 reference:** § 11.10(g).

### URS-P11-021

**Prevent recent password reuse**

> The system must prevent users from reusing any of their previous four passwords.

- **Permanent UUID:** `019f4cbc-ba55-70fb-b757-f203fe319d54`
- **Applicability:** Treat four-password history as an organization-specific example and align the depth with approved identity policy and centralized identity controls.
- **21 CFR Part 11 reference:** § 11.10(g).

### URS-P11-022

**Lock accounts after failed logins**

> After an administratively configurable number of unsuccessful login attempts, the system must lock the account or prevent further login attempts for 30 minutes.

- **Permanent UUID:** `019f4cbc-ba55-70fb-b757-f4e303e4aeee`
- **Applicability:** Treat attempt counts and duration as organization-specific. Assess denial-of-service risk, progressive delay, unlock controls, alerting, emergency access, and identity-provider behavior.
- **21 CFR Part 11 reference:** § 11.10(g); see also § 11.300(d) for electronic-signature credential safeguards.

### URS-P11-023

**Reauthenticate after inactivity**

> The system must force users to reauthenticate or log in again after an administratively configurable period of inactivity.

- **Permanent UUID:** `019f4cbc-ba55-70fb-b757-fbc14c036384`
- **Applicability:** Define the period from use environment, process duration, safety, shared-terminal risk, signature workflow, and identity-provider capability.
- **21 CFR Part 11 reference:** § 11.10(g).

### URS-P11-024

**Provide secure password reset**

> The system must provide a secure mechanism for a user to set a new password after forgetting the current password.

- **Permanent UUID:** `019f4cbc-ba55-70fb-b757-fcdbf52ccd1d`
- **Applicability:** Define identity proofing, reset authorization, token lifetime, notification, audit logging, help-desk controls, temporary credentials, and federated identity ownership.
- **21 CFR Part 11 reference:** § 11.10(g).

### URS-P11-025

**Reset initial password**

> The system must force users to reset their password the first time they log in.

- **Permanent UUID:** `019f4cbc-ba55-70fb-b758-00462b5bb5fa`
- **Applicability:** Apply when temporary or initial passwords are issued. Federated identity, invitation links, passwordless onboarding, or user-created credentials need equivalent controls.
- **21 CFR Part 11 reference:** § 11.10(g).

### URS-P11-026

**Deactivate user access**

> The system must allow an authorized administrator to remove or deactivate a user's access without removing the user's historical attribution.

- **Permanent UUID:** `019f4cbc-ba55-70fb-b758-0592a99684a0`
- **Applicability:** Define authorization, timing, active-session revocation, interfaces, disabled-account retention, reactivation, service accounts, and propagation evidence.
- **21 CFR Part 11 reference:** §§ 11.10(d) and 11.10(g).

### URS-P11-027

**Configure role-based user groups**

> The system must support user groups defined by an approved user-group access matrix, including Operator, Supervisor, Maintenance, and Administrator where applicable.

- **Permanent UUID:** `019f4cbc-ba55-70fb-b758-0b26084b1872`
- **Applicability:** Treat the four role names as examples. Define roles from the actual process, segregation of duties, least privilege, supplier access, and approved access matrix.
- **21 CFR Part 11 reference:** § 11.10(g).

### URS-P11-028

**Enforce data-entry limits**

> The system must prevent data entry outside predefined approved limits.

- **Permanent UUID:** `019f4cbc-ba55-70fb-b758-0e2280d4dd27`
- **Applicability:** Apply only where justified limits exist. Define units, precision, warning versus rejection, overrides, reason capture, interface inputs, device checks, and change control.
- **21 CFR Part 11 reference:** § 11.10(h); related operational checks may also fall under § 11.10(f).

## Electronic signatures

### URS-P11-029

**Display electronic signature manifestation**

> Electronically signed electronic records must contain the printed name of the signer, the date and time the signature was executed, and the meaning associated with the signature.

- **Permanent UUID:** `019f4cbc-ba55-70fb-b758-12ac50680847`
- **Applicability:** Ensure the manifestation remains part of human-readable displays and copies, is linked to the signed record, and uses controlled signature meanings.
- **21 CFR Part 11 reference:** § 11.50(a) and § 11.50(b).

### URS-P11-030

**Authenticate continuous-session signatures**

> During a continuous period of controlled system access, the system must require all electronic-signature components for the first signing and at least one component executable only by the individual for each subsequent signing.

- **Permanent UUID:** `019f4cbc-ba55-70fb-b758-16843f20adb2`
- **Applicability:** Apply to non-biometric signatures during one continuous controlled session. Define how continuous controlled access begins and ends.
- **21 CFR Part 11 reference:** § 11.200(a)(1)(i).

### URS-P11-031

**Authenticate non-continuous-session signatures**

> For a signing outside a single continuous period of controlled system access, the system must require all electronic-signature components for each signing.

- **Permanent UUID:** `019f4cbc-ba55-70fb-b758-18946f10cc5b`
- **Applicability:** Apply to non-biometric signatures outside one continuous controlled session. Verify all required signature components for every signing.
- **21 CFR Part 11 reference:** § 11.200(a)(1)(ii).

### URS-P11-032

**Enforce password aging**

> After an administratively configurable period, the system must force users to change their password.

- **Permanent UUID:** `019f4cbc-ba55-70fb-b758-1e6158234b7f`
- **Applicability:** Define the period from approved identity policy, current security guidance, compromise-detection capability, multifactor authentication, system constraints, and 21 CFR 11.300(b).
- **21 CFR Part 11 reference:** § 11.300(b).

## How to use these records through the API

Retrieve the catalog and filter records where `type` is `urs_requirement`. Each record provides:

- an immutable UUID and editable human label
- normalized and source statements
- rationale and applicability guidance
- contextual criticality
- suggested verification methods
- separate book and current-eCFR references

Use the individual record URL when citing a selected requirement. Preserve its UUID and version in the organization's traceability matrix, then assign an organization-specific requirement identifier and GxP criticality during adoption.
