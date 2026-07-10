---
title: API Quickstart
sidebar_label: Quickstart
api_id: b0ca203e-4b6c-4e9e-8c94-4fcd81341b79
api_type: guidance
api_version: "1.0"
api_status: published
---

# API Quickstart

The API publishes static JSON under `https://www.gxpblueprint.com/api/v1`. No authentication is required.

## Discover the dataset

```bash
curl https://www.gxpblueprint.com/api/v1/manifest.json
```

List records without downloading every Markdown body:

```bash
curl https://www.gxpblueprint.com/api/v1/catalog.json
```

Retrieve one record using its permanent UUID:

```bash
curl https://www.gxpblueprint.com/api/v1/records/dffd5600-0fca-4d87-b435-cbd3ae0f79e7.json
```

## JavaScript

```js
const response = await fetch('https://www.gxpblueprint.com/api/v1/catalog.json');
if (!response.ok) throw new Error(`GxP Blueprint request failed: ${response.status}`);

const catalog = await response.json();
const sops = catalog.records.filter((record) => record.type === 'sop');
```

## Python

```python
import json
from urllib.request import urlopen

with urlopen("https://www.gxpblueprint.com/api/v1/manifest.json") as response:
    manifest = json.load(response)

print(manifest["recordCount"])
```

## Static-resource errors

The initial API consists of static files. A valid record URL returns `200`. An unknown UUID normally returns the hosting provider's `404` response rather than a JSON error body. Clients should check the HTTP status before parsing JSON.

Use the catalog to discover valid records rather than guessing UUIDs.
