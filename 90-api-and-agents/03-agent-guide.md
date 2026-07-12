---
title: Use GxP Blueprint with an AI Agent
sidebar_label: Agent Guide
api_id: b7eaf1e6-c61f-48bc-9516-6c4cb3185388
api_type: guidance
api_version: "1.1"
api_status: published
---

# Use GxP Blueprint with an AI Agent

Give your agent this instruction:

> Read `https://www.gxpblueprint.com/agents/gxp-blueprint.md`, follow its safety rules, and then help me with my GxP task.

The agent needs web access to follow the URL. If it cannot open websites, copy the official instruction file into the conversation or install the `gxp-blueprint` skill package from the repository.

## Useful starting requests

> Find and explain the latest GxP Blueprint Change Control SOP. Include its UUID, version, lifecycle status, and source link.

> Create a draft URS for a configurable cloud training system used to manage GMP training. Keep each requirement independently testable and trace it to the sources used.

> Select applicable Part 11 requirements for an electronic batch-record system. Explain why each source requirement applies, keep source criticality contextual, and identify architecture-specific examples that need adaptation.

> Compare my SOP with the current GxP Blueprint reference. Classify findings as confirmed gap, possible gap, not applicable, or needs review.

> Build a traceability matrix for access control, audit trails, electronic signatures, backup, and record retention.

## What the agent should return

- the exact records it used
- UUID, version, status, and source link for each record
- a distinction between retrieved material and generated recommendations
- assumptions and unresolved applicability questions
- a clear draft and human-review notice for regulated deliverables

Do not paste confidential company records into a public service unless your organization has approved that use. The GxP Blueprint API is read-only and never needs your private content.
