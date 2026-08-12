# Hi, I'm Topu Kumar Mondol

🎓 ECE Undergraduate @ RUET, Bangladesh

 Backend Engineer (Python · FastAPI · PostgreSQL) | AI Systems Builder

I focus on building production-quality backend systems and AI-powered applications — not tutorials, real systems with real design decisions.

---

## Projects

### OpsIQ — AI-Powered Ops Intelligence Platform

> Multi-agent incident investigation system using LangGraph

- Architected a 3-mode AI assistant (Chat, RAG, Automated Postmortem) with a parallel LangGraph pipeline and 3 specialized LLM instances per session

- Validated against 3 real production postmortems — GitLab 2017, Cloudflare 2019, AWS 2020 — root cause category matching confirmed

- Confidence-aware pipeline — halts and asks clarifying questions when evidence score drops below 60%

- Stateless HMAC-SHA256 session tokens with server-side TTL enforcement — sub-millisecond auth latency

- 64 passing tests (unit + integration) · FastAPI · LangGraph · LangChain · FAISS · PostgreSQL · Groq (Llama 3.3 70B)

### ContentPlatform — Personalized Recommendation Engine

> Production-style backend with a 3-tier Softmax explore–exploit algorithm

- 3-tier hybrid ranking: deterministic exploit → Softmax sampling (temp=0.7) → ε-greedy 10% injection — solves filter bubble problem

- Exponential time decay exp(−t/24h) + interaction-weighted category preferences, recalculated every 10 min via background scheduler

- Load-tested with Locust: 99% success rate at 100 concurrent users (~800ms p95)

- 42 tests covering softmax correctness, auth lifecycle, admin RBAC, race-condition prevention

- FastAPI · PostgreSQL · SQLAlchemy 2.0 · JWT + OTP Auth · APScheduler · Pytest · Locust

---

## 🛠️ Tech Stack

**Languages**

<p>

  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>

  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white"/>

  <img src="https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black"/>

  <img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"/>

</p>

**Backend & Database**

<p>

  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white"/>

  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white"/>

  <img src="https://img.shields.io/badge/SQLAlchemy-D71F00?style=for-the-badge&logo=sqlalchemy&logoColor=white"/>

  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>

</p>

**AI / ML**

<p>

  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white"/>

  <img src="https://img.shields.io/badge/LangGraph-FF6B6B?style=for-the-badge&logoColor=white"/>

  <img src="https://img.shields.io/badge/FAISS-007ACC?style=for-the-badge&logoColor=white"/>

</p>

---

## 📚 Certifications

- ✅ Machine Learning Specialization — Andrew Ng / DeepLearning.AI (Coursera)

- ✅ CS50x — Harvard

- ✅ CS50P — Harvard

---

## 📊 GitHub Stats

<p align="center">

  <img src="https://github-readme-stats.vercel.app/api?username=topukumar538&show_icons=true&theme=tokyonight&hide_border=true" width="48%"/>

  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=topukumar538&layout=compact&theme=tokyonight&hide_border=true&hide=html,css&langs_count=6" width="40%"/>

</p>

<p align="center">

  <img src="https://github-readme-streak-stats.herokuapp.com/?user=topukumar538&theme=tokyonight&hide_border=true"/>

</p>

---

## 🎯 Currently

- 📌 Solving 250+ LeetCode problems — arrays, trees, graphs, binary search

---

<p align="center">

  <img src="https://komarev.com/ghpvc/?username=topukumar538&style=flat-square&color=blue"/>

</p>

