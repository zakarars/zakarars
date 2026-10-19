## Arsen Zakaryan

AI automation engineer in Yerevan. I build AI agents, RAG pipelines and business systems for
real companies, deploy them, and keep them running. I make the architecture and design decisions;
most of the implementation is written by AI coding agents I direct (Claude Code, Codex, Gemini).
**C is the language I write unassisted.**

### Public project

**[jira-decisions-mcp](https://github.com/zakarars/jira-decisions-mcp)**: an MCP server that
triages a Jira board with typed, calibrated decisions instead of prose. Python computes the facts
(dates, staleness, blockers); a small local model (Qwen3) makes only the judgment calls (which
team, how urgent). Every answer carries a confidence and a `needs_human_review` flag. It was
evaluated once on a held-out test split: of the 20 tickets it flagged as misfiled, 15 really were.
It runs fully locally, includes a read-only dashboard and has 291 tests. Built on synthetic data.
`Python` `MCP` `Qwen3` `FastAPI` `pytest`

### Production work (client repositories are private)

**AI sales assistant for a real-estate developer**: a multilingual (Armenian / Russian / English)
chatbot that answers availability and pricing questions across 397 units and passes qualified
leads to the sales team. It's an n8n AI agent over Supabase pgvector with Gemini. Retrieval is
mandatory, so it can't invent prices (12 of 12 test answers matched the catalogue). It has retries,
an error workflow with throttled Telegram alerts, and a staged daily sync, so a failed data load
never breaks the live bot.
`n8n` `LangChain` `Gemini` `pgvector` `Telegram`

**Oil station management platform**: inventory, clients, sales, role-based access control and
audit logging behind an Armenian-language interface. Five services under Docker Compose
(PostgreSQL 16, backend, frontend, Telegram bot, Caddy with TLS). In daily use.
`Python` `aiogram` `Docker Compose` `Caddy` `PostgreSQL`

**[carstar.am](https://carstar.am)**: vehicle-import pricing platform for the Armenian market.
It turns a US auction price into a full landed cost: customs duty, VAT, three shipping legs and
live Central Bank exchange rates, with an admin dashboard for leads and inventory. 851 commits over
about 17 months. The site is up; the pricing backend is currently offline.
`React/TypeScript` `FastAPI` `Supabase` `GitHub Actions`

**Internal AI tools at CleanWhale (Prague)**: a Telegram documentation assistant (Python + Gemini
API) for staff. I chose topic routing over vector search because, at that corpus size, vector
search added complexity without improving accuracy. Privacy was built in: a data-sharing notice,
scope limits, 6-month auto-deletion and a lawyer-drafted consent document. Also a 61-test
Playwright/pytest monitoring suite running every 6 hours with Telegram alerts.

### Background

Before engineering full-time I coordinated a ~120-person service operation across Prague and
Brno, so I start from the business problem and agree on how "working" will be measured before
building.

### Contact

[arsen.zakaryan@gmail.com](mailto:arsen.zakaryan@gmail.com) ·
[LinkedIn](https://linkedin.com/in/arsen-zakaryan-964968133)
