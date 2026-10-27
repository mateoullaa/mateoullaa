# Hi, I'm Mateo Ulla 👋

<p align="left">
  <img src="https://img.shields.io/badge/Software%20Developer-1E1E1E?style=flat-square&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/AI%20%26%20Automation-0A66C2?style=flat-square&logo=openai&logoColor=white" />
  <img src="https://img.shields.io/badge/Cybersecurity-3A7CA5?style=flat-square&logo=shield&logoColor=white" />
  <img src="https://img.shields.io/badge/Data%20Analysis-1F7A1F?style=flat-square&logo=python&logoColor=white" />
</p>

## About Me

Developer focused on building production-grade systems at the intersection of **AI, automation, and data**.

I design and develop projects end-to-end — from architecture to Docker deployment — with a focus on clean engineering: deterministic logic, fail-safe design, and thorough testing. Currently building AI-powered tools for real operational problems in security, finance, and developer tooling.

## Tech Stack

<p align="left">
  <!-- Programming Languages -->
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white" />
  <img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white" />

  <!-- AI / ML -->
  <img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white" />
  <img src="https://img.shields.io/badge/ChromaDB-FF6B35?style=flat-square&logo=databricks&logoColor=white" />
  <img src="https://img.shields.io/badge/Claude%20Code-D97757?style=flat-square&logo=anthropic&logoColor=white" />

  <!-- Backend -->
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white" />
  <img src="https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white" />

  <!-- Frontend -->
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" />
  <img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white" />
  <img src="https://img.shields.io/badge/Bootstrap-7952B3?style=flat-square&logo=bootstrap&logoColor=white" />

  <!-- Data & DevOps -->
  <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" />
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />
  <img src="https://img.shields.io/badge/Pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white" />
  <img src="https://img.shields.io/badge/VS%20Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white" />
  <img src="https://img.shields.io/badge/Figma-F24E1E?style=flat-square&logo=figma&logoColor=white" />
</p>

## Featured Projects

---

### 🔷 Prism — AI-Powered SOC Alert Triage Agent

> `Python` · `FastAPI` · `Ollama (local LLM)` · `ChromaDB` · `Docker` · `VirusTotal / AbuseIPDB / OTX`

On-premise AI agent that automates the first triage layer of a Security Operations Center. Receives Wazuh alerts via webhook, classifies them, enriches indicators of compromise with three threat intelligence APIs in parallel, and uses a **local LLM** to produce a structured verdict — MITRE ATT&CK mapping, risk score, and recommended next action. Routes alerts to TheHive 5 via Shuffle SOAR.

**v2.2:** RAG pipeline with ChromaDB + Ollama embeddings — retrieves the N most similar historical alerts and injects them as context into the LLM prompt. Auto-classifying false positives from those precedents runs in shadow mode: it logs what it would do, without acting, until the corpus is large enough to validate it.

- **~7 min → 12–15 s** first-pass triage per alert (~97%); designed from **6,320 real production alerts**
- Production-deployed in Docker, wired end-to-end: Wazuh → Prism → TheHive
- **334 deterministic tests**, zero network required (all external APIs mocked)
- Metrics dashboard: `GET /dashboard` (Chart.js) + `GET /metrics` (JSON audit stats)
- All inference runs locally — no alert data leaves the network

🔗 [github.com/mateoullaa/prism](https://github.com/mateoullaa/prism)

---

### 🧮 Axiom — Deterministic Trading Strategy Builder

> `Python` · `FastAPI` · `Pydantic v2` · `pandas` · `backtesting.py` · `React` · `Tailwind`

Builds trading strategies from a closed catalog of objective rules, lints them, exports each one as a standalone Python file, and backtests that exact file on real market data.

- **No AI at runtime:** the same inputs always produce the same strategy
- 70/30 out-of-sample split; every result is published, including the ones that lose to buy & hold
- **93 tests**, CI on GitHub Actions

🔗 [github.com/mateoullaa/axiom](https://github.com/mateoullaa/axiom)

---

### 🧩 Claude Code Project Harness — Self-Improving Agentic Coding Framework

> `Claude Code` · `Python` · `Agent Orchestration`

A pair of Claude Code Skills that turn a blank folder into a structured, self-improving development agent — with a real verification loop, not just a longer system prompt. Separates deterministic execution from agent orchestration (Planner → Builder → Reviewer → Scribe), enforces a hard review gate before any task is marked done, and logs every failure to a running memory file so the agent keeps improving within a project over time.

🔗 [github.com/mateoullaa/Claude-Code-Project-Harness](https://github.com/mateoullaa/Claude-Code-Project-Harness)

---

### 📊 Token Dashboard — Local Claude Code Usage Analytics

> `Python (stdlib only)` · `SQLite` · `Vanilla JS` · `ECharts`

Local, read-only dashboard that reads Claude Code's own transcript logs and turns them into per-prompt cost analytics, cache-efficiency metrics, tool/file usage heatmaps, and a live activity feed. 100% local — no telemetry, no external API calls, no login, no build step.

🔗 [github.com/mateoullaa/Token-Dashboard-](https://github.com/mateoullaa/Token-Dashboard-)

---

## Other Projects

| Project | Description | Stack |
|---|---|---|
| [Claude Plugins](https://github.com/mateoullaa/Claude-Plugins) | Curated, security-vetted collection of Skills, Agents, and `CLAUDE.md` configs for Claude Code. | — |
| [Aula Virtual](https://github.com/mateoullaa/Aula-Virtual) | Virtual classroom platform — courses, exams, messaging, role-based dashboards. | Flask · MySQL |
| [App de Cobro](https://github.com/mateoullaa/App-de-cobro) | E-commerce demo with Mercado Pago payment integration. | Flask |
| [App Copa Renault](https://github.com/mateoullaa/App-Copa-Renault) | Tournament management system — teams, fixtures, and roles. | Flask · Bootstrap |
| [Taller Mecánico Django](https://github.com/mateoullaa/Taller-Mecanico-Django-V2) | Management system for a mechanical workshop — clients, vehicles, billing. | Django · MySQL |
| [Algorithmic Trading Research](https://github.com/mateoullaa/TRADING-ALGORITMICO) | SMA-200 backtest research on the S&P 500 with position sizing and risk management. | Python |
| [BTC Strategy Tester](https://github.com/mateoullaa/BTC-STRATEGY-TESTER) | Streamlit app to backtest BTC/USDT strategies against historical data, with PDF reports. | Streamlit · Binance API |

---

## How I Work

- **End-to-end ownership** — I design, build, test, and deploy. From architecture decisions to Docker containers in production.
- **AI & local inference** — local LLMs (Ollama), vector search (ChromaDB), RAG pipelines, without sending data to external services.
- **Engineering discipline** — deterministic logic over probabilism, fail-safe design, mocked test suites. No half-finished implementations.
- **Real operational context** — Prism was deployed in a production SOC and validated against live alerts; its design came from 6,320 real ones.

## Interests

- AI engineering and automation
- Cybersecurity and threat intelligence
- Finance and quantitative analysis
- Building tools with real operational value
- Gym

## Contact

- [GitHub](https://github.com/mateoullaa)
- [LinkedIn](https://www.linkedin.com/in/mateoulla/)

---
