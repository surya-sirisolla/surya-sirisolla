# Hi, I'm S Jaya Surya 👋

📍 Hyderabad, India  |  ⚡ Backend Engineer + Agent Systems  |  🤖 LLMs, MCP, GRPO  |  🚀 Distributed Systems @ Reliance Jio

---

Backend engineer with **~4 years** building high-scale, fault-tolerant systems — and increasingly, the **AI agent layer** on top of them.

Currently at **QuEST Global (Reliance Jio)**, where I architected real-time monitoring infrastructure for live IPL 2025 broadcasts, and built an in-house **agent platform on OpenClaw + MCP** that lets stakeholders query production logs and project status from WhatsApp/RCS — cutting manual ops effort by 60%+.

On the side, I train LLMs to act like coordinated on-call teams (multi-agent RLVR with GRPO), run agents on-device with llama.cpp, and care a lot about latency, reliability, and AI features that hold up in production rather than just demos.

---

## 🛠️ Stack

**Backend & Distributed Systems**
[![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)]()
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)]()
[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)]()
[![gRPC](https://img.shields.io/badge/gRPC-4285F4?style=flat-square&logo=google&logoColor=white)]()
[![Kafka](https://img.shields.io/badge/Kafka-000000?style=flat-square&logo=apachekafka)]()
[![Flink](https://img.shields.io/badge/Flink-E6526F?style=flat-square&logo=apacheflink&logoColor=white)]()
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)]()
[![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)]()
[![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)]()
[![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?style=flat-square&logo=elasticsearch&logoColor=white)]()

**AI / Agents**
[![MCP](https://img.shields.io/badge/MCP-FF6F61?style=flat-square)]()
[![OpenClaw](https://img.shields.io/badge/OpenClaw-6A1B9A?style=flat-square)]()
[![Koog](https://img.shields.io/badge/Koog-2E7D32?style=flat-square)]()
[![llama.cpp](https://img.shields.io/badge/llama.cpp-000000?style=flat-square)]()
[![GRPO](https://img.shields.io/badge/GRPO%20%2F%20RLVR-FFA500?style=flat-square)]()
[![Hugging Face](https://img.shields.io/badge/HuggingFace-FFD21F?style=flat-square&logo=huggingface&logoColor=black)]()
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)]()

**Cloud & Observability**
[![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)]()
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)]()
[![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)]()
[![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)]()
[![Kibana](https://img.shields.io/badge/Kibana-005571?style=flat-square&logo=kibana&logoColor=white)]()

---

## 🔨 What I've Built

### 🤖 LogSentinel v2 — Multi-Agent SOC Simulator *(Meta Hackathon — Top 800 / 50,000+ teams)*
A research environment for training LLMs to handle long-horizon incident response as a coordinated SOC team — not single-turn classifiers.

- **4 specialized agents** (Incident Commander, App SRE, DB SRE, Security Analyst) with partial observability and a shared handoff board
- **5-phase action-driven lifecycle:** DETECT → TRIAGE → MITIGATE → VERIFY → FINAL_REPORT
- Latent world-state model — only evidence-backed mitigations move the needle; blind guessing is penalized
- **Trained Qwen2.5-7B via GRPO** (TRL + Unsloth) with adaptive curriculum
- Composite reward (outcome + detection F1 + severity + efficiency + teamwork) with **4 anti-reward-hacking penalties**
- **Ships as an OpenEnv-compliant FastAPI server** — runs locally, in Docker, or on a Hugging Face Space
- **Benchmarked:** 0.49 avg reward vs 0.41 heuristic baseline. Resolves incidents in **8 steps vs 45**.

→ [github.com/surya-sirisolla/log-env](https://github.com/surya-sirisolla/log-env)

---

### 📱 On-Device Mobile Agent *(Koog + llama.cpp)*
A fully offline personal agent that runs on my phone. No cloud round-trip, no API costs, full data privacy.

- **Koog agent framework** with **llama.cpp** for on-device inference
- Benchmarked **SmolLM2 (350M/700M)**, **LFM2.5 (350M/700M)**, and **Qwen2 0.5B** for tool-calling latency and accuracy on mobile hardware
- Agent queries the **device messaging database** via tool calls to: summarize conversations, surface missed deals or important messages, and track personal spending

→ [github.com/surya-sirisolla](https://github.com/surya-sirisolla)

---

### 🔴 Real-Time Monitoring — IPL 2025 *(QuEST Global × Reliance Jio)*
Architected the entire backend from scratch for one of the biggest live streaming events on the planet.

- **Stack:** Go, gRPC, Kafka, Flink, Elasticsearch
- Zero ad-delivery downtime across live matches
- **API latency: 20s → 1s** (95% improvement)
- **Mistral 7B** integrated into the observability pipeline to auto-summarize error clusters → 20% faster incident triage
- Custom log analytics engine + frontend observability views → 40% faster RCA

---

### 💬 Conversational Agent Platform — OpenClaw + MCP *(Reliance Jio)*
Built an agentic system on top of the production Jio backend. Exposes project services and Elasticsearch-backed log analytics as **MCP server tools**, with **WhatsApp** and **RCS** as conversational channels.

- Stakeholders query project status and pull logs from any device, no dashboards needed
- **Cut manual operational and support effort by 60%+** across Jio Business Messaging and adjacent projects
- Built on a fork of OpenClaw — see [nanoclaw](https://github.com/surya-sirisolla/nanoclaw)

---

### 🍽️ MaMenu — QR-Based Restaurant Ordering *(Side Product)*
A contactless digital menu and hotel operations platform.

- **Go** backend, **Next.js** frontend
- Full RBAC, end-to-end table & order management

→ [github.com/surya-sirisolla/ma-menu](https://github.com/surya-sirisolla/ma-menu)

---

### 🛒 E-commerce & 🏥 Healthcare Platforms *(Udify Technologies)*
- **E-commerce:** Modular auth APIs in Nest.js + TypeScript. Razorpay + custom wallet with 100% transaction integrity.
- **Healthcare:** High-performance scheduling APIs on PostgreSQL. Automated billing validation — 20% fewer errors. Granular RBAC on AWS.

---

### 📚 LeetCode Top 150 — DSA Interview Notes
Pattern-based markdown notes for all 150 LeetCode Top Interview questions. Covers 16 patterns: Arrays, Two Pointers, Sliding Window, Trees, Graphs, DP, and more. Each problem includes intuition, approach, pseudocode, complexity analysis, and key pattern takeaways.

→ [github.com/surya-sirisolla/leetcode-top-150](https://github.com/surya-sirisolla/leetcode-top-150)

---

## 🏆 Highlights

- 🥇 **Partner Award** — Reliance Jio
- 🌟 **Rising Star** — QuEST Global
- ⚡ **2× On-the-Fly Awards** — QuEST Global
- 🏅 **Meta Hackathon — Top 800 / 50,000+ teams (Round 1 qualifier)**
- 📉 **95% API latency reduction** in production (20s → 1s)
- 🤖 **60%+ reduction in manual ops effort** via the OpenClaw + MCP agent platform

---

## 📫 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jaya-surya-sirisolla-1926b6200/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:suryasirisolla@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=vercel&logoColor=white)](https://sirisolla-surya.web.app/)

*Open to senior backend, AI/agent engineering, and LLM systems roles — Hyderabad, Bangalore, or remote.*
