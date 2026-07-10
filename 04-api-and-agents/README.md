---
title: API and AI Agents
sidebar_label: API and AI Agents
api_id: 079011fc-22d6-41fa-ae7d-1dda8795e46a
api_type: collection
api_version: "1.0"
api_status: published
---

# API and AI Agents

Use the public GxP Blueprint API to retrieve the same open-reference material published on this site. The initial API is read-only, requires no account or API key, and is designed for software integrations and AI agents.

## Start without writing code

Give a web-enabled agent this address:

```text
https://www.gxpblueprint.com/agents/gxp-blueprint.md
```

Then describe the task, for example:

> Use GxP Blueprint to help me draft a URS for a cloud-based GMP training system. Preserve the source references and explain what needs human review.

If your agent cannot open links, copy the instructions from the [agent guide](./03-agent-guide.md) into the conversation.

## Build an integration

- Follow the [quickstart](./01-quickstart.md).
- Review the [content model](./02-content-model.md).
- Read the [agent guide](./03-agent-guide.md).
- Understand [security, limits, and fair use](./04-security-and-limits.md).
- Download the [OpenAPI 3.1 description](https://www.gxpblueprint.com/api/v1/openapi.json).

## Important limitation

GxP Blueprint provides reference material. It does not know your organization's products, processes, licences, validation state, risk controls, or approval system. Adapt generated material and obtain appropriate subject-matter and Quality review before use.

The dataset currently declares its license as `NOASSERTION` because this repository does not yet contain a formal licence declaration. Do not infer reuse rights beyond published repository terms.
