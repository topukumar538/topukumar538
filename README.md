# Hi, I'm Topu Kumar Mondol

ECE Undergraduate @ RUET '28, Bangladesh
Backend Engineer (Python · FastAPI · PostgreSQL) | AI Systems Builder

I build production-quality backend systems and AI-powered applications — real systems with real design decisions, not tutorials.

[LinkedIn]({LINKEDIN_URL}) · [Email](mailto:{EMAIL})

---

## Projects

### OpsIQ — AI-Powered Ops Intelligence Platform
> Multi-agent incident investigation system built on LangGraph

[Code]({OPSIQ_REPO_URL}) · [Live Demo]({HUGGINGFACE_SPACE_URL}) · [Architecture]({OPSIQ_REPO_URL}#architecture)

![CI]({OPSIQ_REPO_URL}/actions/workflows/ci.yml/badge.svg)

- Architected a 3-mode assistant (Chat, RAG, Automated Postmortem) on a LangGraph StateGraph pipeline: `log_agent → rootcause_agent → remediation_agent`
- Validated against 3 real production postmortems — GitLab 2017, Cloudflare 2019, AWS us-east-1 2020 — with root cause category matching confirmed
- Confidence-aware pipeline halts and asks clarifying questions when the evidence score drops below 60%, rather than emitting a low-confidence root cause
- Stateless HMAC-SHA256 session tokens with server-side TTL enforcement — no session table, horizontally scalable
- Containerized with Docker and deployed to Hugging Face Spaces with a hosted Postgres backend (Neon)
- 64 passing tests (unit + integration)

**Stack:** FastAPI · LangGraph · LangChain · FAISS · PostgreSQL · SQLAlchemy 2.0 · Docker · Groq (Llama 3.3 70B)

### ContentPlatform — Personalized Recommendation Engine
> Production-style backend with a 3-tier softmax explore–exploit ranking algorithm

[Code]({CONTENTPLATFORM_REPO_URL}) · [Live Demo]({CONTENTPLATFORM_DEMO_URL})

- 3-tier hybrid ranking: deterministic exploit → softmax sampling (temp=0.7) → ε-greedy 10% injection, to counter filter-bubble collapse
- Exponential time decay `exp(−t/24h)` with interaction-weighted category preferences, recalculated every 10 minutes via a background scheduler
- Load-tested with Locust at 100 concurrent users: ~800ms p95 latency
- 42 tests covering softmax correctness, auth lifecycle, admin RBAC, and race-condition prevention

**Stack:** FastAPI · PostgreSQL · SQLAlchemy 2.0 · JWT + OTP Auth · APScheduler · Pytest · Locust

---

## Tech Stack

**Languages** — Python · C++ · C · SQL
**Backend** — FastAPI · PostgreSQL · SQLAlchemy 2.0 · REST APIs · Docker
**AI / ML** — LangChain · LangGraph · FAISS · RAG pipelines
**Tools** — Git · GitHub Actions · Pytest · Locust · Linux

---

## Certifications

- Machine Learning Specialization — DeepLearning.AI (Andrew Ng)
- CS50x — Harvard
- CS50P — Harvard

---

## Currently

- 250+ LeetCode problems solved — arrays, trees, graphs, binary search
- Preparing for Summer 2027 SWE internship applications
- Microsoft Learn Student Ambassador

---

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=topukumar538&layout=compact&theme=tokyonight&hide_border=true&hide=html,css&langs_count=6" width="40%"/>
</p>
