
# 🛰️ MDT — Mobile Dispatch & Tracking System

> **Multi-Agent Android Platform for Real-Time Live Tracking, Smart Dispatch & Operational Intelligence**

![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?style=flat-square&logo=android&logoColor=white)
![Status](https://img.shields.io/badge/Status-PRD%20v2.5-blue?style=flat-square)
![Architecture](https://img.shields.io/badge/Architecture-Multi--Agent%20System-purple?style=flat-square)
![Hackathon](https://img.shields.io/badge/Event-The%20Invasion%20Hackathon-FF6B6B?style=flat-square)
![Author](https://img.shields.io/badge/Author-Rangesh%20Gupta-0A66C2?style=flat-square&logo=linkedin)

---

## 📌 Overview

**MDT (Mobile Dispatch & Tracking)** is a next-generation Android application designed to solve real-world problems in live field operations — logistics, fleet management, emergency dispatch, and workforce tracking. Built around a **multi-agent AI orchestration system**, MDT delivers real-time situational awareness, smart task assignment, and predictive decision-making directly on mobile.

This repository contains the **Product Requirements Document (PRD) v2.5** — the full technical blueprint for the MDT Android system, covering architecture design, feature specifications, agent workflows, API contracts, and UX flow.

---

## 🎯 Problem Statement

Traditional dispatch and field tracking systems suffer from:

- **Siloed data** — no real-time visibility across field agents and operations center
- **Manual decision-making** — dispatchers manually assign tasks without AI assistance
- **Reactive responses** — problems are addressed after they occur, not predicted in advance
- **Poor mobile-first UX** — legacy web dashboards repurposed for mobile with poor ergonomics

MDT solves all four with an AI-native, mobile-first architecture.

---

## 🚀 Key Features

### 🗺️ Live Tracking Engine
- Real-time GPS tracking with sub-5 second position updates
- Route deviation detection and smart re-routing alerts
- Geofence triggers with configurable entry/exit notifications
- Historical route playback with time-scrubbing

### 🤖 Multi-Agent AI System
- **Dispatch Agent** — auto-assigns tasks to nearest available field unit based on skill, proximity, and workload
- **Monitoring Agent** — continuously scans active operations for anomalies and escalates alerts
- **Prediction Agent** — uses historical patterns to forecast delays, demand spikes, and resource gaps
- **Communication Agent** — orchestrates team notifications, escalations, and status broadcasts
- Agents operate concurrently with a central orchestrator managing priority and conflict resolution

### 📱 Android-Native UX
- Optimized for single-hand use in field conditions
- Offline-first architecture — core features work without connectivity
- Live sync on reconnect with conflict resolution
- Dark mode and high-contrast accessibility support

### 📊 Operational Dashboard
- Real-time KPI cards: active units, task completion rate, avg response time
- Heat maps for activity density across geographic zones
- Agent performance analytics with trend graphs
- Exportable reports in PDF and CSV

### 🔔 Smart Notification System
- Priority-based notification queue — critical alerts bypass Do Not Disturb
- In-app actionable notifications (approve/reject/reassign without leaving notification shade)
- Push + WebSocket dual delivery for zero notification loss

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                     MDT Android Client                      │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────────┐  │
│  │  Live Map UI │  │  Task Board  │  │  Agent Console   │  │
│  └──────┬───────┘  └──────┬───────┘  └────────┬─────────┘  │
│         └─────────────────┴──────────────────┘             │
│                        ↕ WebSocket / REST                   │
└─────────────────────────────────────────────────────────────┘
                              ↕
┌─────────────────────────────────────────────────────────────┐
│                    MDT Backend Orchestrator                  │
│  ┌────────────┐ ┌──────────────┐ ┌───────────┐ ┌────────┐  │
│  │  Dispatch  │ │  Monitoring  │ │ Prediction│ │  Comms │  │
│  │   Agent    │ │    Agent     │ │   Agent   │ │ Agent  │  │
│  └────────────┘ └──────────────┘ └───────────┘ └────────┘  │
│                   Central Orchestrator                       │
└─────────────────────────────────────────────────────────────┘
                              ↕
┌─────────────────────────────────────────────────────────────┐
│              Data Layer: PostgreSQL + Redis + S3             │
└─────────────────────────────────────────────────────────────┘
```

---

## 🛠️ Tech Stack (Planned)

| Layer | Technology |
|-------|-----------|
| **Mobile** | Android (Kotlin + Jetpack Compose) |
| **Live Tracking** | Google Maps SDK, Fused Location Provider |
| **Real-Time Sync** | WebSocket (OkHttp / Socket.IO) |
| **Multi-Agent AI** | Gemini 2.5 Flash API + Custom Orchestrator |
| **Backend** | Node.js / FastAPI (Python) |
| **Database** | PostgreSQL + Redis (caching + pub/sub) |
| **Push Notifications** | Firebase Cloud Messaging (FCM) |
| **Authentication** | Firebase Auth / JWT |
| **Storage** | AWS S3 / Firebase Storage |
| **Analytics** | Custom dashboards + Mixpanel |

---

## 📄 Repository Contents

| File | Description |
|------|-------------|
| `MDT_Android_PRD_v2.5_LiveTracking_MultiAgent.docx` | Full Product Requirements Document — v2.5 covering all features, architecture diagrams, API specs, agent workflows, UX wireframe descriptions, and acceptance criteria |

---

## 📋 PRD Document Highlights (v2.5)

The PRD covers:

- **Executive Summary** — product vision, target users, success metrics
- **Feature Specifications** — detailed user stories and acceptance criteria for all modules
- **Agent Workflow Diagrams** — decision trees for all 4 AI agents
- **API Contract** — REST + WebSocket endpoint definitions
- **Data Models** — entity relationships for users, tasks, routes, geofences
- **UX Flow** — screen-by-screen user journey maps
- **Performance Requirements** — latency, uptime, and sync benchmarks
- **Security & Privacy** — data handling, encryption, and compliance specifications
- **Rollout Plan** — MVP scope, Phase 1, Phase 2 feature breakdown

---

## 🏆 Hackathon Context

This project was conceived and the PRD was authored for **The Invasion Hackathon** — a competitive hackathon focused on building AI-powered operational tools. The PRD represents a complete product blueprint ready for engineering execution.

**Key innovations pitched:**
- First Android dispatch system with fully autonomous multi-agent task orchestration
- Sub-5s live tracking with offline resilience
- Gemini 2.5 Flash integration for on-device AI decision support

---

## 👤 Author

**Rangesh Gupta**
- 🎓 B.E. Computer Engineering (Data Science) — SLRTCE, Mumbai (2025–2029)
- 🤖 Google Student Ambassador 2026
- 💼 Aspiring Data Analyst | AI Builder
- 🔗 [LinkedIn](https://linkedin.com/in/rangesh-gupta) | [GitHub](https://github.com/rangeshsha-Rookie)

---

## 📜 License

This project and its PRD document are the intellectual property of Rangesh Gupta. All rights reserved.

---

*Built with precision. Designed for real-world impact. 🚀*
