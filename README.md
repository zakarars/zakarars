## Arsen Zakaryan

Independent software consultant, Yerevan. I design the systems I ship, make the architectural
decisions and keep them running in production. The implementation is written by AI coding agents
I direct — Claude Code, Codex, Gemini. **C is the language I write unassisted.**

### What I've built

**[carstar.am](https://carstar.am)** — vehicle-import pricing platform for the Armenian market,
live and public. Turns a US auction price into a full landed cost: customs duty, VAT, three-leg
shipping, live Central Bank exchange rates. The core of it is Armenia's vehicle import tax and
customs regulations reverse-engineered into a working pricing engine. Admin dashboard for leads,
pricing and inventory. *851 commits over ~17 months, in production.*
`React/TypeScript` `FastAPI` `Supabase/PostgreSQL` `GitHub Actions` `Vercel` `Railway`

**Oil station management platform** — inventory, clients, sales, role-based access control and
audit logging behind an Armenian-language interface. Five services under Docker Compose:
PostgreSQL 16, backend, frontend, Telegram bot, Caddy reverse proxy with TLS.
*731 commits over 3 months, still active.*
`Python` `aiogram` `Docker Compose` `Caddy` `PostgreSQL 16`

**Regression and monitoring suite** — 61 Playwright/pytest end-to-end tests over business-critical
flows on mobile and desktop, running every 6 hours in GitHub Actions, alerting to Telegram with
screenshots on failure.
`Playwright` `pytest` `GitHub Actions`

**Telegram documentation assistant** (at CleanWhale) — Python and the Gemini API, answering staff
questions from internal documentation. Routing-based retrieval: documentation segmented into topic
files, the relevant one selected via the system prompt. I evaluated an embeddings/vector-search
pipeline and turned it down — at that corpus size it would have added complexity without improving
accuracy.
`Python` `aiogram` `Google Gemini API`

### Why most of this isn't here

The systems above are client work in private repositories, so what's public on this account is
mostly older learning material. carstar.am is live if you want to see the real thing, and I'm happy
to walk through architecture and decisions in a conversation.

### Also

~120-person service operation coordinated across Prague and Brno at CleanWhale, alongside building
the internal tooling it ran on. I scope, price and write my own client proposals.

Learning projects on this account, listed as such: a Vertex AI chatbot on Cloud Run, a RAG document
assistant with ChromaDB, a voice assistant chaining Google Cloud STT → Gemini → TTS, and a retrieval
bot in Go. Prototypes, not production systems.

### Reach me

[arsen.zakaryan@gmail.com](mailto:arsen.zakaryan@gmail.com) ·
[LinkedIn](https://linkedin.com/in/arsen-zakaryan-964968133)
