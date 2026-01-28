---
title: GxP Standards Glossary
sidebar_label: Glossary
---

# GxP Standards Glossary

A unified dictionary defining both traditional pharmaceutical validation terms and modern software engineering concepts used in the GxP Blueprint.

## Core GxP Terms

| Term                    | Definition                                    | Key Context                                                                                                                              |
| :---------------------- | :-------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------- |
| **ALCOA+**              | The standard for Data Integrity.              | Data must be **A**ttributable, **L**egible, **C**ontemporaneous, **O**riginal, **A**ccurate + Complete, Consistent, Enduring, Available. |
| **CFR**                 | Code of Federal Regulations (US Law).         | **21 CFR Part 11:** Electronic Records & Signatures.<br/>**21 CFR Part 210/211:** GMP for Manufacturing.                                 |
| **CSA**                 | Computer Software Assurance.                  | The FDA's modern, risk-based approach. Prioritizes critical thinking and testing over massive documentation.                             |
| **CSV**                 | Computer System Validation.                   | The traditional "GAMP 5" V-Model process. Often associated with heavy documentation and manual screenshots.                              |
| **GxP**                 | Good [Something] Practice.                    | **GMP:** Manufacturing<br/>**GLP:** Laboratory<br/>**GCP:** Clinical<br/>**GDP:** Distribution                                           |
| **IQ / OQ / PQ**        | The traditional 3-stage validation lifecycle. | **IQ:** Installation (Is it built right?)<br/>**OQ:** Operation (Does it function?)<br/>**PQ:** Performance (Does it work under load?)   |
| **QMS**                 | Quality Management System.                    | The master system of processes, procedures (SOPs), and responsibilities for achieving quality policies.                                  |
| **Traceability Matrix** | A map of Requirements to Tests.               | Ensures every single User Requirement has a corresponding Test Case.                                                                     |

## Modern Engineering Terms

| Term                  | Definition                              | Relevance to GxP                                                                                           |
| :-------------------- | :-------------------------------------- | :--------------------------------------------------------------------------------------------------------- |
| **CI/CD**             | Continuous Integration / Deployment.    | Automates the "IQ" and "OQ" phases by running test scripts on every code change.                           |
| **Git**               | Distributed Version Control.            | Provides a cryptographically secure, immutable audit trail of exactly who changed what and when.           |
| **IaC**               | Infrastructure as Code.                 | Eliminates "server drift." Ensures the "Qualified State" of a server can be reproduced instantly via code. |
| **Pull Request (PR)** | A code review request.                  | Acts as the "Pre-Approval" step in a Change Control. Merging the PR is the "Approval."                     |
| **Unit Testing**      | Testing individual software components. | High unit test coverage reduces the reliance on manual, black-box OQ scripts.                              |
