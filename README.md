# Ansvar Gateway

**EU regulatory intelligence over MCP — law, regulations, standards & threat intel, every answer cited or refused.**

Ansvar Gateway is a **remote MCP server** for compliance, legal, and security work. One OAuth connection gives your agent scoped `search` and `get_provision` across audited European law corpora (27 jurisdictions live), the EU regulations corpus (GDPR, NIS2, DORA, AI Act, CRA — 98 instruments), 262 security frameworks, and live CVE/KEV/EPSS intelligence.

Every result carries a source citation (`_citation`: URL, publisher, licence) — answers are cited from fetched text or explicitly refused, never guessed from model memory. Paid tiers add full-fleet fan-out, case law / preparatory works / agency guidance, and structured workflows (DPIA, STRIDE/LINDDUN, gap analysis) that return exportable deliverables.

## Connect

| | |
|---|---|
| **Endpoint** | `https://gateway.ansvar.eu/mcp` (streamable HTTP) |
| **Auth** | OAuth 2.1 with Dynamic Client Registration — no API keys |
| **Registry** | [`eu.ansvar/gateway`](https://registry.modelcontextprotocol.io/v0/servers?search=eu.ansvar%2Fgateway) in the official MCP registry |
| **Quickstart** | https://ansvar.eu/docs/quickstart |
| **Setup guides** (Claude, Copilot Studio, Gemini, custom clients) | https://ansvar.eu/setup |
| **Pricing** | Free tier (B2B signup, 100 searches/day) → https://ansvar.eu/pricing |
| **Coverage** | https://ansvar.eu/coverage |
| **Privacy policy** | https://ansvar.eu/privacy |
| **Terms** | https://ansvar.eu/terms |
| **llms.txt** | https://ansvar.eu/llms.txt |

Claude Desktop / Claude Code / any MCP client that supports remote servers: add `https://gateway.ansvar.eu/mcp` as a remote MCP server and complete the OAuth flow. Free-tier signup is in-flow.

## What your agent can do

- `search` legislation, regulations, standards and threat intel across jurisdictions — results return matching provisions with article-level citations, not paraphrases.
- `get_provision` / `get_decision` — resolve a canonical reference to the exact provision or court decision text.
- `list_coverage` — discover what corpora and jurisdictions are live, by domain.
- Premium tiers: automatic case-law / preparatory-works fan-out inside `search`, agency guidance, and workflow prompts that produce finished, cited deliverables (DPIA, threat model, gap analysis).

## Trust properties

- **Accuracy over availability:** if a source is unreachable, the gateway returns a data-source-unavailable error — it never answers from model memory.
- **Per-item attribution:** every served row carries source URL, publisher, and licence; content with unresolved licensing is withheld with an explicit notice, not silently dropped.
- **EU-hosted** (Hetzner, Germany/Finland), no server-side model, no tracking. Operated by [Ansvar Systems AB](https://ansvar.eu) (Sweden, org.nr 559547-2225).

## About this repository

This is the public home of the hosted Ansvar Gateway — documentation and listing anchor only; the gateway service itself is not developed in this repository. Open-source law-connector code lives across the [Ansvar-Systems](https://github.com/Ansvar-Systems) organization (Apache-2.0).

Issues and questions are welcome here; commercial contact: https://ansvar.eu/contact.
