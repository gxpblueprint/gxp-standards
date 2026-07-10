---
title: Content Model, Identity, and Versions
sidebar_label: Content Model
api_id: 3dd31995-1dd1-44f7-9b5e-8e4425ab3462
api_type: guidance
api_version: "1.1"
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
    "sourcePath": "docs/01-quality-systems/02-change-control/01-sop-change-management.md",
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

The current dataset contains SOPs, guidance, and collection pages. The common contract also reserves separate schemas for:

- `urs_requirement`: an independently addressable, testable requirement with its own UUID
- `checklist`: structured actions and expected evidence
- `template`: a reusable content template

A future URS document and the reusable requirements it contains must not share one identifier. Each independently cited requirement receives its own UUID and type-specific fields such as statement, rationale, GxP criticality, verification method, and regulatory references.
