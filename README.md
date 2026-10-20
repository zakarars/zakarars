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

### Case studies

**[zakarars/case-studies](https://github.com/zakarars/case-studies)**: write-ups of five client
systems, each with the problem, architecture diagrams, the key decisions, measured results, real
screenshots and a short animated walkthrough:
[CBS sales assistant](https://github.com/zakarars/case-studies/tree/main/cbs-sales-assistant) ·
[Auto-parts shop CRM](https://github.com/zakarars/case-studies/tree/main/autoparts-crm) ·
[Har Oil station platform](https://github.com/zakarars/case-studies/tree/main/oil-station-platform) ·
[carstar pricing engine](https://github.com/zakarars/case-studies/tree/main/carstar-pricing-engine) ·
[CleanWhale QA monitor and assistant](https://github.com/zakarars/case-studies/tree/main/cleanwhale-internal-ai)

### Production work (client repositories are private)

**AI sales assistant for a real-estate developer**: a multilingual (Armenian / Russian / English)
chatbot that answers availability and pricing questions across 397 units and passes qualified
leads to the sales team. It's an n8n AI agent over Supabase pgvector with Gemini. Retrieval is
mandatory before any figure: in test rounds the agent looked the catalogue up 12 of 12 times (was
3 of 6) and all 14 quoted figures were real. It has retries,
an error workflow with throttled Telegram alerts, and a staged daily sync, so a failed data load
never breaks the live bot.
`n8n` `LangChain` `Gemini` `pgvector` `Telegram`

**Auto-parts shop CRM with fiscal receipts**: parts, stock per location, sales, client debts,
suppliers and a car-service module for a live shop, in Armenian, Russian and English. A small bridge
program on the shop PC sends each sale to the physical fiscal register over the tax authority's
protocol; a request with no clear answer is marked UNKNOWN and never re-sent automatically. Live
since Sep 2026, 572 tests.
`Python` `Flask` `PostgreSQL` `Docker Compose` `Alpine.js`

**Oil station management platform (Har Oil)**: inventory, clients, sales, role-based access control and
audit logging behind an Armenian-language interface. Five services under Docker Compose
(PostgreSQL 16, backend, frontend, Telegram bot, Caddy with TLS). In daily use.
`Python` `aiogram` `Docker Compose` `Caddy` `PostgreSQL`

**[carstar.am](https://carstar.am)**: vehicle-import pricing platform for the Armenian market.
It turns a US auction price into a full landed cost: customs duty, VAT, three shipping legs and
live Central Bank exchange rates, with an admin dashboard for leads and inventory. 860+ commits,
Dec 2025 – Jun 2026. The site is up; the pricing backend is currently offline.
`React/TypeScript` `FastAPI` `Supabase` `GitHub Actions`

**Internal AI tools at CleanWhale (Prague)**: a Telegram documentation assistant for partner
cleaners: FastAPI on Cloud Run, LangChain retrieval over a FAISS index of 19 topic documents, and
Gemini, with a secret-token webhook, Secret Manager and `pip-audit` in every build. Also a 66-test
Playwright/pytest suite that ran against the live booking site every 6 hours (Feb – Mar 2026),
calibrated on 5 real bugs, with Telegram alerts that show the failing element outlined.
`Python` `LangChain` `FAISS` `Gemini` `Cloud Run` `Playwright`

### Background

Before engineering full-time I coordinated a ~120-person service operation across Prague and
Brno, so I start from the business problem and agree on how "working" will be measured before
building.

### Contact

[arsen.zakaryan@gmail.com](mailto:arsen.zakaryan@gmail.com) ·
[LinkedIn](https://linkedin.com/in/arsen-zakaryan-964968133)
