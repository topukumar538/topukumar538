# Hi, I'm Topu Kumar Mondol

🎓 ECE Undergraduate @ RUET '28, Bangladesh
Backend Engineer (Python · FastAPI · PostgreSQL) | AI Systems Builder

I build production-quality backend systems and AI-powered applications — real systems with real design decisions, load-tested, containerized and shipped through CI.

📄 [Resume](https://topukumar538.github.io) · 💼 [LinkedIn](https://linkedin.com/in/topu-kumar-mondol) · ✉️ topukumar538@gmail.com

---

## Projects

### OpsIQ — AI-Powered Ops Intelligence Platform
> Multi-agent incident investigation system built on a LangGraph DAG

[Code]({OPSIQ_REPO_URL}) · [Live Demo]({HUGGINGFACE_SPACE_URL})

- **5-node LangGraph DAG** — log analysis and timeline extraction run in parallel and join at root-cause inference, over three temperature-tuned LLM instances (0.7 chat / 0.3 RAG / 0.1 postmortem) isolating generative, grounded and deterministic work
- **Verified against 3 documented production incidents** — GitLab 2017, Cloudflare 2019, AWS 2020 — replayed through the pipeline, asserting both root-cause category matches and domain-specific terms drawn from the published postmortems
- **Stateless HMAC-SHA256 session tokens** carrying a version field — bumping one database column invalidates every issued token, with the server storing none of them
- **Restart-transparent state** — FAISS stores persisted to disk under per-user, per-session paths and conversation state mirrored to PostgreSQL, so summary buffers and recent messages survive a reconnect
- **Confidence-aware pipeline** — halts and asks clarifying questions when the evidence score drops below 60%
- **123-test GitHub Actions pipeline** runs on every push and deploys only when tests pass, replacing manual redeploys

`FastAPI` · `LangGraph` · `LangChain` · `FAISS` · `PostgreSQL (async SQLAlchemy)` · `Groq (Llama 3.3 70B)` · `Docker` · `Neon`

### ContentPlatform — Personalized Recommendation Engine
> Production-style backend with a slot-based explore–exploit ranker

[Code]({CONTENTPLATFORM_REPO_URL}) · [Live Demo]({CONTENTPLATFORM_DEMO_URL})

- **99% success rate at 100 concurrent users (~800ms p95)** — load tested with Locust from 10 to 500 users, and root-caused the failure at 500 as database connection pool exhaustion
- **No single category dominates the feed** — capped at 3 of the top 5 slots per page by a slot-based ranker using softmax sampling at temp=0.7 with 10% random injection
- **Recommendations follow current behaviour, not old activity** — interaction weights (view=1, like=3, save=5) decayed on a 30-day constant and recomputed for every user in hourly batches
- **Zero repeats across the entire feed** — all pages built in one pass against a shared seen-set, seeded so pagination stays stable at a full 20 posts per page
- **Admin blocks apply in one request instead of up to 7 days** — user state re-checked in the database on every authenticated request rather than trusted from the JWT
- **58-test GitHub Actions pipeline** automating deployment to Hugging Face Spaces

`FastAPI` · `PostgreSQL` · `SQLAlchemy 2.0` · `JWT + OTP Auth` · `APScheduler` · `Docker` · `Pytest` · `Locust`

**Also:** [Regulated Power Distribution System](https://github.com/Md-Yousuf-2723/Regulated_Power_Distribution) — STM32-based embedded team project at RUET, built with [@Md-Yousuf-2723](https://github.com/Md-Yousuf-2723) and Anindita Sarkar.

---

## 🛠️ Tech Stack

**Languages**
<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white"/>
  <img src="https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black"/>
  <img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"/>
</p>

**Backend & Databases**
<p>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/SQLAlchemy-D71F00?style=for-the-badge&logo=sqlalchemy&logoColor=white"/>
  <img src="https://img.shields.io/badge/Pydantic-E92063?style=for-the-badge&logo=pydantic&logoColor=white"/>
</p>

**AI / ML**
<p>
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white"/>
  <img src="https://img.shields.io/badge/LangGraph-FF6B6B?style=for-the-badge&logoColor=white"/>
  <img src="https://img.shields.io/badge/FAISS-007ACC?style=for-the-badge&logoColor=white"/>
  <img src="https://img.shields.io/badge/RAG-6E4AFF?style=for-the-badge&logoColor=white"/>
</p>

**Cloud & Infrastructure**
<p>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white"/>
  <img src="https://img.shields.io/badge/Hugging_Face_Spaces-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black"/>
  <img src="https://img.shields.io/badge/Neon-00E599?style=for-the-badge&logo=postgresql&logoColor=black"/>
</p>

**Tools**
<p>
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white"/>
  <img src="https://img.shields.io/badge/Pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white"/>
  <img src="https://img.shields.io/badge/Locust-2EA44F?style=for-the-badge&logoColor=white"/>
</p>

---

## 🎓 Education

**Rajshahi University of Engineering & Technology (RUET)** — B.Sc. in Electrical & Computer Engineering
Expected Oct 2028 · CGPA 3.51 / 4.00
Coursework: Data Structures & Algorithms, Object-Oriented Programming, Database Systems

---

## 📚 Certifications

- ✅ **Machine Learning Specialization** — DeepLearning.AI / Andrew Ng (Coursera) · Dec 2025
- ✅ **CS50x: Introduction to Computer Science** — HarvardX (edX) · Oct 2024
- ✅ **CS50P: Introduction to Programming with Python** — HarvardX (edX) · 2024

---

## 🎯 Currently

- 📌 **400+ DSA problems solved** across LeetCode, GeeksforGeeks and Codeforces — arrays, trees, graphs, binary search, dynamic programming
- ☁️ Working through AWS fundamentals
- 🌱 Preparing for open-source contributions in the CNCF ecosystem (Prometheus, OpenTelemetry)
- 💼 Open to **Summer 2027 Software Engineering internships**

---

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=topukumar538&show_icons=true&theme=tokyonight&hide_border=true" width="48%"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=topukumar538&layout=compact&theme=tokyonight&hide_border=true&hide=html,css&langs_count=6" width="40%"/>
</p>
<p align="center">
  <img src="https://streak-stats.demolab.com?user=topukumar538&theme=tokyonight&hide_border=true"/>
</p>
