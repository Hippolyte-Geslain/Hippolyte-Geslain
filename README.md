<!-- Hippolyte Geslain — GitHub profile -->

<h1 align="center">Hippolyte Geslain</h1>

<p align="center">
  <strong>AI engineer · Marseille</strong><br/>
  <em>I build AI that doesn't phone home.</em>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/hippolyte-geslain/"><img src="https://img.shields.io/badge/LinkedIn-hippolyte--geslain-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <img src="https://img.shields.io/badge/open_to-AI_engineer_roles-2ea44f?style=flat-square" alt="Open to AI engineer roles"/>
</p>

---

Most AI demos send your data to someone else's server and hope for the best.
My clients can't do that: an accounting firm can't upload its customers' invoices, a company can't paste its secrets into a chatbot.

So I bring the model to the data. **Local LLMs, document AI, retrieval and agents**, built for real clients at the AI Lab of [La Plateforme_](https://laplateforme.io), measured against real data and shipped in Docker.

```text
if the data can't leave the building:
    the model comes to the data
```

## Selected work

> Client projects are private. These are short case studies, without names.

**Invoice compliance, fully on-premise** · *lead developer and architect*<br/>
An accounting firm spends about two days per client checking that invoices carry the mentions the law requires.
I built the system that reads native and scanned invoices and extracts zones, with page and position kept as proof for each value. A consultant reviews everything in a back-office. No invoice leaves the firm: OCR and a local NuExtract model run on its own GPU.
`Python` `docling` `llama-server` `Docker GPU` `Caddy` · 45 architecture decision records, 72 test files.

**Tech watch that reads 30 sources so a team doesn't have to** · *solo*<br/>
For a 30-person web agency: daily ingestion of about 30 tech sources, LLM summaries **with cited sources**, a 09:30 digest in Google Chat, and a RAG chatbot over the same corpus. Built and run entirely on free tiers, which meant pacing every rate limit and moving hosts when one closed its door.
`n8n` `Postgres + pgvector` `Gemini` `FastAPI` `Render`

**Supplier catalogues, normalised by an LLM** · *main developer, team of 3*<br/>
Excel, PDF and CSV files from many suppliers turned into one product format: the LLM maps the columns, then an async web search fills missing EAN codes and compositions, with the source kept for every value.
`Flask` `pandas` `OpenRouter` `Docker` `CapRover`

**AI-maturity diagnostic for small businesses** · *application owner*<br/>
A 15-question self-assessment that scores a company, recommends training and books a meeting. I rewrote the application and built the email and CRM flow.
`FastAPI` `HubSpot` `Brevo` `Kubernetes / FluxCD`

## Open source

| Project | What it is |
|---|---|
| **[Lumen](https://github.com/Hippolyte-Geslain/lumen)** | A local-first desktop cockpit: board, notes, inbox, calendar. One click hands a task to a Claude Code agent working in its own git worktree, and a bundled llama.cpp keeps everything else on your machine. `Tauri` `Node` `SQLite` `llama.cpp` |
| **[AutoStartUper](https://github.com/Hippolyte-Geslain/autostartuper)** | Tells a French entrepreneur what to file, when, and links the government page that says so. One rule: every fact comes from an official source. The AI stays at the edges and never decides what you owe. `Next.js` `TypeScript` · 393 tests |
| **[DocSortR](https://github.com/Hippolyte-Geslain/DocSortR)** | Drop in administrative documents and get them OCR'd, classified by a local LLM and filed by client, type and year. Works 100% offline. `Electron` `FastAPI` `Ollama` |
| **[MealMatch](https://github.com/Hippolyte-Geslain/mealder)** | Build a menu by swiping through recipes, and import new recipes from a photo or a PDF. `Expo` `React Native` `SQLite` |

## How I work

- **Measure first.** Every extraction pipeline gets a test set with known answers before it gets a new prompt.
- **Write the decision down.** Architecture decision records, runbooks, handover documents.
- **AI at the edges.** The model reads, drafts and suggests. Rules, money and legal answers stay deterministic and sourced.
- **Nothing leaves without permission.** Outgoing calls go through an allow-list, and secrets are encrypted and never shown to the model.

## Toolbox

**AI** · local LLMs (llama.cpp, llama-server, Ollama), RAG (pgvector, ChromaDB), OCR and document AI (docling, RapidOCR), agents and MCP, Claude Code<br/>
**Backend** · Python, FastAPI, Flask, SQLAlchemy, PostgreSQL, SQLite, n8n<br/>
**Frontend and apps** · TypeScript, React, Next.js, Electron, Tauri, Expo<br/>
**Shipping** · Docker, CapRover, Render, Kubernetes / FluxCD, GitHub Actions<br/>
**Data** · pandas, R, Power BI, scikit-learn

<details>
<summary><strong>Off the clock</strong></summary>
<br/>

- I train AI developers: I co-run an AI-integrator course and designed a training on AI agents for a company.
- This README was written in a Markdown vault that indexes itself with local embeddings and is managed by Claude Code. Old habits.
- Teamfight Tactics, ranked Master. Good practice for decisions under uncertainty.

</details>
