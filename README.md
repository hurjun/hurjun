<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=180&section=header&text=Heojun%20Hur&fontSize=64&fontAlignY=36&desc=Full-Stack%20Developer%20%C2%B7%20Ships%20Real%20Products%20End%20to%20End&descAlignY=58&descSize=22" />
</div>

<div align="center">
  <a href="mailto:hurjun96@gmail.com"><img src="https://img.shields.io/badge/Email-hurjun96@gmail.com-D14836?style=flat&logo=Gmail&logoColor=white" /></a>
  &nbsp;
  <a href="https://linkedin.com/in/jun-hur-a3b0b7159"><img src="https://img.shields.io/badge/LinkedIn-Heojun%20Hur-0A66C2?style=flat&logo=LinkedIn&logoColor=white" /></a>
  &nbsp;
  <a href="https://github.com/hurjun"><img src="https://img.shields.io/badge/GitHub-hurjun-181717?style=flat&logo=GitHub&logoColor=white" /></a>
</div>

<br>

### About

I'm a **full-stack web developer**, and my signature strength is **diagnosing and fixing a wide
variety of errors across the entire stack** — frontend, backend, database, infrastructure,
real-time links, and robotics telemetry. When something breaks in production, I'm the person who
traces it from the browser to the socket to the query plan and makes it stay fixed.

Over **5+ years** I've built and shipped production systems across **robotics, fintech, and
healthcare** — as a solo developer owning everything end to end, and as the web lead for fleets of
real robots in the field. One principle guides everything I ship:

> **The value of a system is determined not just by its capability, but by how well it fits the
> actual workflows, habits, and needs of the people who use it.**

So I design from the user's real workflow inward — the data model, the API, the UI, the real-time
link, and the operational tooling — and I take ownership of all of it. Because a system only
delivers value when it stays up, the work I'm proudest of is the least glamorous one: **I've solved
a wide variety of errors across the entire stack.**

---

### Shipped Products

Production systems I built and shipped — each one is run by real companies.

| Product | What it is | Stack | Live |
|---|---|---|---|
| **CRISK** | Corporate carbon / climate-risk reporting platform — auto-generated risk reports backed by FastAPI financial-data endpoints and Spring Boot auth. | FastAPI · Spring Boot · MySQL · AWS | [crisk.co.kr](https://www.crisk.co.kr/) |
| **Credivalue** | Asynchronous Excel-processing reporting service — AWS Lambda + Step Functions + SQS pipeline for large uploads. | AWS Lambda · Step Functions · SQS | [credivalue.com](https://credivalue.com/) |
| **Credit Imbalance Tracker** | Credit-imbalance tracking dashboard over collected financial data, built for enesg. | Next.js · Node.js · TypeScript · MUI | [enesg.co.kr](http://www.enesg.co.kr/) |
| **Gole FMS Console** | End-to-end Fleet Management System for AMR robot swarms — live map, scenario editor, cargo tracking, and role-based ops console. | React · TypeScript · PostgreSQL · MQTT · VDA5050 | *Operator console (internal)* |

---

### 🔧 Debugging & Reliability

> The thread that runs through every job below: finding the failure, naming it precisely, and
> engineering the system so it survives the next one.

- **Performance — report generation 10 min → 2 min.** At Niflers I profiled and optimized a
  monolithic **20,000+ line** report-generation script, cutting end-to-end runtime from
  **10 minutes to 2 minutes**.
- **Anticipation — MQTT anomalies that predicted failures.** At Dogu Robotics I discovered that
  **abnormal shifts in MQTT message frequency often predicted robot failures *before* customers
  noticed them**, and turned that signal into proactive monitoring across 30+ deployed robots.
- **Classification — network vs. auth vs. DB.** At Gole Robotics I built logging that **cleanly
  separates network, authentication, and database failures**, paired with **WebSocket auto-backoff
  reconnection** and **render throttling** so the real-time fleet UI survives flaky links instead
  of falling over.
- **Whole-stack ownership.** As Niflers' **solo** full-stack developer I personally diagnosed and
  fixed failures across *every* layer — frontend, backend, database, infrastructure, and
  deployment — and **migrated a live frontend from Vue.js to React without breaking deployed
  sites**.

---

### Experience

#### 🤖 Gole Robotics — Full-Stack & Robotics Simulation Engineer · *2024.05 – Present (current)*

Building an end-to-end **Fleet Management System (FMS)** for AMR swarms (deployment + service robots).

- Real-time fleet control over **MQTT / VDA5050**, with **WebSocket** feeds using snapshot +
  incremental updates, render throttling, and auto-backoff reconnection for flaky links.
- **Visual scenario editor** — operators compose routes over SLAM maps and directional navigation
  nodes.
- **Cargo tracking** — automated photography, pickup/dropoff history, per-robot throughput
  analytics, recurring schedules, and multi-floor delivery with elevator coordination.
- **Role-based access control** + comprehensive logging on a **PostgreSQL** backend that
  distinguishes network / auth / DB failures.
- **Sim-to-Real** workflows with NVIDIA **Isaac Sim/Lab**, reinforcement learning, and domain
  randomization.
- *Stack: React · TypeScript · PostgreSQL · MQTT · VDA5050*

#### 💹 Niflers — Full-Stack Engineer (solo) · Fintech / Climate Risk · *2024.01 – 2025.11*

Single developer owning **all** frontend, backend, infrastructure, and deployment.

- Optimized a monolithic **20,000+ line** script: report generation **10 min → 2 min**.
- Auto-generation system for **200K+** corporate carbon-risk reports.
- **MySQL** schema design + automated **daily data-collection pipeline** (Docker + Nginx).
- **FastAPI** financial-data endpoints + **Spring Boot** authentication for crisk.co.kr.
- **AWS ECS + Step Functions** parallel pipeline for daily financial-data ingestion.
- **LLM-based** natural-language report Q&A prototype.
- Shipped **CRISK**, **Credivalue**, and the **enesg Credit Imbalance Tracker** (see table above).

#### 🦾 Dogu Robotics — Robot Control System Developer & Web Lead · *2022.01 – 2023.12*

Real-time monitoring and control for **30+ robots across 10+ sites** (hospital, outdoor, factory).

- **WebRTC** video streaming + **MQTT** control/monitoring + **Grafana** dashboards.
- Discovered that **MQTT message-frequency anomalies predicted failures before customer
  complaints**, enabling proactive monitoring.
- Migrated the frontend **Vue.js → React** with standardized components across deployments.
- Service-robot front-facing touch UI — wayfinding, info display, real-time **Zoom SDK** video calls.
- Organized developer conferences and study groups (Git, clean code, engineering culture).
- *Clients: Hyundai · SK Hynix · GS EPS*

#### 🏭 Mobile Entropy — Full-Stack Developer · *2021.05 – 2021.11*

Built the Incheon City Gas **ERP** system.

#### 🌊 NSG Co., Ltd. — Freelance, Digital Twin · *2021.03 – 2021.04*

Converted K-water (Korea Water Resources Corp) nuclear **thermal-hydraulic** calculation logic into
a **C++ digital twin**.

---

### Technical Skills

<div align="center">

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=Python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=TypeScript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=JavaScript&logoColor=black)
![Java](https://img.shields.io/badge/Java-007396?style=flat&logo=openjdk&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white)

**Frontend**

![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=React&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=Next.js&logoColor=white)
![Vue.js](https://img.shields.io/badge/Vue.js-4FC08D?style=flat&logo=vuedotjs&logoColor=white)
![MUI](https://img.shields.io/badge/MUI-007FFF?style=flat&logo=mui&logoColor=white)

**Backend**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=FastAPI&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat&logo=SpringBoot&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-000000?style=flat&logo=express&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-5FA04E?style=flat&logo=nodedotjs&logoColor=white)

**Cloud / Infra**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=AmazonWebServices&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=Docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat&logo=nginx&logoColor=white)

**Databases**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=MySQL&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat&logo=mariadb&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle-F80000?style=flat&logo=oracle&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=Redis&logoColor=white)

**Real-time / Systems**

![WebSocket](https://img.shields.io/badge/WebSocket-010101?style=flat&logo=socketdotio&logoColor=white)
![MQTT](https://img.shields.io/badge/MQTT-660066?style=flat&logo=MQTT&logoColor=white)
![WebRTC](https://img.shields.io/badge/WebRTC-333333?style=flat&logo=WebRTC&logoColor=white)
![VDA5050](https://img.shields.io/badge/VDA5050-1F6FEB?style=flat)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white)

**Robotics / ML** *(secondary)*

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=PyTorch&logoColor=white)
![ROS](https://img.shields.io/badge/ROS%2FROS2-22314E?style=flat&logo=ros&logoColor=white)
![Isaac Sim](https://img.shields.io/badge/Isaac%20Sim%2FLab-76B900?style=flat&logo=nvidia&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=flat&logo=nvidia&logoColor=white)

</div>

---

### Open-Source & From-Scratch

Secondary to the production work above: reproducible repositories where I re-derive core algorithms
from the papers and measure them, rather than wrap a library. Every number below is quoted directly
from that repo's own README.

| Repository | What it is | Headline result |
|---|---|---|
| [**mapf-fleet**](https://github.com/hurjun/mapf-fleet) | From-scratch **TypeScript MAPF** engine (windowed cooperative A\* / WHCA\*, Conflict-Based Search), 3D fleet sim, capacity-limited elevators, fleet-size optimizer. | **0 collisions** across **66** seed-swept runs / **21,000+** ticks; **~9.3 deliveries/min** at 16 agents. |
| [**mlops** · PPE Watchman](https://github.com/hurjun/mlops) | YOLOv8 edge detector → FastAPI hub → WebSocket Next.js live dashboard; offline-first edge-to-cloud event pipeline. | **33 passing tests** over a distributed event pipeline (edge inference → aggregation → live browser). |
| [**attention_is_all_you_need**](https://github.com/hurjun/attention_is_all_you_need) | From-scratch PyTorch **Transformer** (multi-head attention, sinusoidal encodings, Noam warmup, label smoothing). | **98.2%** greedy exact-match on a synthetic reverse task, reproducible in **~90 s on CPU**. |
| [**xLSTM**](https://github.com/hurjun/xLSTM) | From-scratch **sLSTM / mLSTM** cells (exponential gating, matrix memory) — NeurIPS 2024. | **100%** on 64-step recall, where a vanilla LSTM stays at chance. |
| [**speculative-decoding-lab**](https://github.com/hurjun/speculative-decoding-lab) | Distribution-preserving **speculative decoding** with acceptance sampling. | **Up to 1.80×** lossless speedup (MPS), output token-for-token identical to autoregressive decoding. |
| [**stock-forecast-benchmark**](https://github.com/hurjun/stock-forecast-benchmark) | **Leakage-aware** benchmark of 9 forecasters behind one interface, with an auto-generated leaderboard. | Apples-to-apples on held-out data — **Prophet leads** over LSTM, GRU, XGBoost, and a Transformer. |
| [**stt-nursing-system** · MediVoice](https://github.com/hurjun/stt-nursing-system) | Voice-first nursing-documentation app (React / TypeScript) turning bedside rounds into structured records. | Study showed **up to 96%** documentation-time reduction. |

**More:** [**open3d**](https://github.com/hurjun/open3d) — 7-stage point-cloud / LiDAR pipeline ·
[**opencv**](https://github.com/hurjun/opencv) — Faster R-CNN person detector + ROI rule engine ·
[**setpoint**](https://github.com/hurjun/setpoint) — RL-from-scratch HVAC control ·
[**gre**](https://github.com/hurjun/gre) — adaptive GRE practice (FastAPI + React + MySQL) ·
[**futurescole**](https://github.com/hurjun/futurescole) — containerized telemetry pipeline (Python + PostgreSQL + Docker).

---

### Education

**B.S. Computer Science**, Chungnam National University · *2016.03 – 2025.02*

---

<div align="center">

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=hurjun&layout=compact&hide_border=true" />
&nbsp;
<img src="https://github-readme-stats.vercel.app/api?username=hurjun&show_icons=true&hide_border=true" />

<br><br>

[![Solved.ac Profile](http://mazassumnida.wtf/api/v2/generate_badge?boj=hurjun96)](https://solved.ac/hurjun96)

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=100&section=footer" />

</div>
