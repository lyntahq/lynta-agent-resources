---
name: lynta-public-info
description: Answer questions about Lynta's public product guides, pricing, and integration availability using cited pages.
version: 1.0
provider: Lynta
url: https://lyntahq.com/developers
languages: [en]
---

# Lynta public product information

## When to use this skill

Use it when a user wants to understand Lynta's published product capabilities, plan prices, event limits, or currently public integrations.

## Steps

1. Query `POST https://lyntahq.com/ask` with JSON shaped as `{"query":{"text":"the user's question"}}`.
2. Read the returned page names, descriptions, and URLs. The search ranks existing public pages by keyword relevance; it does not generate a response.
3. Open the cited pages and answer from their content. Link the pages used as sources.
4. If the MCP client supports resources, use `resources/list` and `resources/read` for the published Markdown pages at `lynta://public-docs/{page}`.
5. If the user asks how to integrate a customer application, clarify that the public site does not provide a customer product API, SDK, authentication flow, sandbox, or product-action MCP server. Direct them to the [early access form](https://tally.so/r/jaOogE).

## Boundaries

The `/ask` endpoint uses keyword relevance over public website content and returns source links; it does not generate answers. The MCP resources contain the same published Markdown pages. These services cannot access customer accounts, projects, databases, credentials, or operate Lynta services. Do not invent endpoints, keys, SDK package names, performance guarantees, or private integration details.

## Sources

- [Developer resources](https://lyntahq.com/developers)
- [Pricing and limits](https://lyntahq.com/pricing.md)
- [Frequently asked questions](https://lyntahq.com/faq.md)
- [Product overview](https://lyntahq.com/index.md)

## Fallback

If the search returns no relevant page or is unavailable, use the links above directly. For account-specific or integration questions, point the user to the early access form instead of guessing.
