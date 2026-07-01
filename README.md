# Hi, I'm Mateo Ulla 👋

<p align="left">
  <img src="https://img.shields.io/badge/Software%20Developer-1E1E1E?style=flat-square&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/AI%20%26%20Automation-0A66C2?style=flat-square&logo=openai&logoColor=white" />
  <img src="https://img.shields.io/badge/Cybersecurity-3A7CA5?style=flat-square&logo=shield&logoColor=white" />
  <img src="https://img.shields.io/badge/Data%20Analysis-1F7A1F?style=flat-square&logo=python&logoColor=white" />
</p>

## About Me

Developer focused on building production-grade systems at the intersection of **AI, automation, and data**.

I design and develop projects end-to-end — from architecture to Docker deployment — with a focus on clean engineering: deterministic logic, fail-safe design, and thorough testing. Currently building AI-powered tools for real operational problems in security and finance.

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

  <!-- Backend -->
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white" />
  <img src="https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" />

  <!-- Frontend -->
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" />
  <img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white" />
  <img src="https://img.shields.io/badge/Bootstrap-7952B3?style=flat-square&logo=bootstrap&logoColor=white" />

  <!-- DevOps & Tools -->
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />
  <img src="https://img.shields.io/badge/Pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white" />
  <img src="https://img.shields.io/badge/VS%20Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white" />
  <img src="https://img.shields.io/badge/Figma-F24E1E?style=flat-square&logo=figma&logoColor=white" />
</p>

## Projects

---

### 🔷 Prism — AI-Powered SOC Alert Triage Agent

> `Python` · `FastAPI` · `Ollama (local LLM)` · `ChromaDB` · `Docker` · `VirusTotal / AbuseIPDB / OTX`

On-premise AI agent that automates the first triage layer of a Security Operations Center. Receives Wazuh alerts via webhook, classifies them, enriches indicators of compromise with three threat intelligence APIs in parallel, and uses a **local LLM** to produce a structured verdict — MITRE ATT&CK mapping, risk score, and recommended next action. Routes alerts to TheHive 5 via Shuffle SOAR.

**v2.2:** RAG pipeline with ChromaDB + Ollama embeddings — retrieves the N most similar historical alerts and injects them as context into the LLM prompt. Shadow-mode auto-classification: when past precedents are unanimously FALSE_POSITIVE at high similarity, the system skips the LLM entirely (~15s saved per alert).

- Production-deployed in Docker, wired end-to-end: Wazuh → Prism → TheHive
- **334 deterministic tests**, zero network required (all external APIs mocked)
- Metrics dashboard: `GET /dashboard` (Chart.js) + `GET /metrics` (JSON audit stats)
- All inference runs locally — no alert data leaves the network

🔗 [github.com/mateoullaa/prism](https://github.com/mateoullaa/prism)

---

### 📈 Algorithmic Trading Research

> `Python` · `Data Analysis` · `Strategy Backtesting`

Trading strategy research and experimentation — quantitative analysis applied to financial markets.

🔗 [github.com/mateoullaa/TRADING-ALGORITMICO](https://github.com/mateoullaa/TRADING-ALGORITMICO)

---

### 🔧 Django Mechanical Workshop System

> `Python` · `Django` · `Web Application`

Full-stack web application for managing a mechanical workshop: client records, service orders, and billing.

🔗 [github.com/mateoullaa/Taller-Mecanico-Django-V2](https://github.com/mateoullaa/Taller-Mecanico-Django-V2)

---

### 🌐 Portfolio Website

Personal portfolio showcasing projects and technical background.

🔗 [portfolio-mateo-ulla.onrender.com](https://portfolio-mateo-ulla.onrender.com/)

---

## How I Work

- **End-to-end ownership** — I design, build, test, and deploy. From architecture decisions to Docker containers in production.
- **AI & local inference** — local LLMs (Ollama), vector search (ChromaDB), RAG pipelines, without sending data to external services.
- **Engineering discipline** — deterministic logic over probabilism, fail-safe design, mocked test suites. No half-finished implementations.
- **Real operational context** — Prism runs in a live SOC environment processing production security alerts daily.

## Interests

- AI engineering and automation
- Cybersecurity and threat intelligence
- Finance and quantitative analysis
- Building tools with real operational value
- Gym

## Contact

- [GitHub](https://github.com/mateoullaa)
- [Portfolio](https://portfolio-mateo-ulla.onrender.com/)
