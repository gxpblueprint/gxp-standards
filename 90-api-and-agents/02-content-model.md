---
title: Content Model, Identity, and Versions
sidebar_label: Content Model
api_id: 3dd31995-1dd1-44f7-9b5e-8e4425ab3462
api_type: guidance
api_version: "1.2"
api_status: published
---

# Content Model, Identity, and Versions

Every public resource is a record with a common envelope and type-specific content.

```json
{
  "id": "dffd5600-0fca-4d87-b435-cbd3ae0f79e7",
  "type": "sop",
  "label": "01-SOP-CCM",
  "title": "Change Control Management",
  "version": "1.0",
  "status": "published",
  "aliases": [],
  "provenance": {
    "sourcePath": "docs/01-quality-systems/01-sops/change-control.md",
    "license": "LicenseRef-GxP-Blueprint-Community-1.0",
    "licenseUrl": "https://www.gxpblueprint.com/licensing",
    "attributionRequired": true
  },
  "links": {
    "canonical": "https://www.gxpblueprint.com/docs/quality-systems/change-control/sop-change-management",
    "api": "https://www.gxpblueprint.com/api/v1/records/dffd5600-0fca-4d87-b435-cbd3ae0f79e7.json"
  },
  "content": {
    "format": "markdown",
    "markdown": "# 01-SOP-CCM: Change Control Management..."
  },
  "contentHash": "sha256:..."
}
```

## Permanent identity

`id` is the immutable UUID of the logical record. Titles, labels, paths, and URLs may change without changing this UUID. Do not use `label` as a database key.

`aliases` can retain former human labels. A build fails if a public record has a missing, invalid, or duplicate UUID.

## Versions and hashes

`version` is the human-readable revision. `contentHash` identifies the exact public representation and changes whenever public metadata or content changes. Build timestamps are excluded from record hashes.

The v1 static API publishes the current source-controlled revision. Historical revision endpoints are reserved for a later release; use repository history when exact earlier revisions are needed today.

## Record types

The current dataset contains SOPs, guidance, collection pages, and independently addressable URS requirements. The common contract provides separate schemas for:

- `urs_requirement`: a populated, independently addressable requirement with normalized and source statements, rationale, applicability, contextual criticality, verification methods, and references
- `checklist`: structured actions and expected evidence
- `template`: a reusable content template

A URS collection page and the reusable requirements it describes do not share one identifier. Each independently cited requirement has its own UUID. Human labels such as `URS-P11-001` remain separate from identity and may evolve without replacing that UUID.

Reusable requirements use `contextual` criticality until an adopting organization assesses intended use, record and signature scope, predicate rules, and risk. Agents and integrations must review the applicability guidance instead of treating the collection as a universal checklist.

Example `urs_requirement` content:

```json
{
  "statement": "The system must be capable of detecting audit trail entries that have been altered since they were originally generated.",
  "sourceStatement": "The system must be capable of detecting any audit trails entries that have been altered since they were originally generated. (Only include this requirement if your system is capable of doing this.)",
  "rationale": "Supports validation of the system's ability to discern invalid or altered records.",
  "applicability": "Include only when the selected system can detect alteration of previously generated audit trail entries.",
  "category": "audit-trail-integrity",
  "gxpCriticality": "contextual",
  "verificationMethods": ["test", "analysis"],
  "references": [
    {
      "kind": "regulation",
      "source": "21 CFR Part 11 - Electronic Records; Electronic Signatures",
      "locator": "§ 11.10(a)",
      "url": "https://www.ecfr.gov/current/title-21/part-11/section-11.10"
    }
  ]
}
```
