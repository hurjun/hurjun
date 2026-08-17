<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=180&section=header&text=Jun%20Hur&fontSize=64&fontAlignY=36&desc=Software%20Reliability%20for%20Cyber-Physical%20Systems&descAlignY=58&descSize=20" />
</div>

<div align="center">
  <a href="https://hurjun.github.io"><img src="https://img.shields.io/badge/Portfolio-hurjun.github.io-0A192F?style=flat&logo=githubpages&logoColor=white" /></a>
  &nbsp;
  <a href="mailto:hurjun96@gmail.com"><img src="https://img.shields.io/badge/Email-hurjun96@gmail.com-D14836?style=flat&logo=Gmail&logoColor=white" /></a>
  &nbsp;
  <a href="https://linkedin.com/in/jun-hur-a3b0b7159"><img src="https://img.shields.io/badge/LinkedIn-Jun%20Hur-0A66C2?style=flat&logo=LinkedIn&logoColor=white" /></a>
</div>

<br>

### About

I build software that keeps robot fleets running in the real world. Over **5+ years** I have
shipped production systems across **robotics, fintech, and healthcare** — robot fleet-control
platforms, financial data pipelines, and clinical software. I currently build the fleet
management system for autonomous mobile robots at **GoLe Robotics** and validate robot behavior
in **NVIDIA Isaac Sim** before deployment.

I am **applying to US CS master's programs** to study the **reliability of cyber-physical
systems** — fault diagnosis, failure prediction, and simulation-based validation — with the goal
of continuing on to a PhD.

**→ [Portfolio with demos and screenshots](https://hurjun.github.io)** ·
[Undergraduate thesis (PDF)](https://hurjun.github.io/asset/graduation_paper.pdf)

---

### Research Interests

Three questions, each of which I first met as an operational problem in production:

1. **Fault diagnosis across system layers.** In the fleets I operated, a single command crossed
   the control frontend, backend, MQTT broker, robot ROS stack, and site network — and failures
   rarely respected those boundaries. I am interested in observability and fault-localization
   techniques that trace causes across layers.
2. **Failure prediction from operational telemetry.** At DOGU Robotics I found that anomalies in
   MQTT message frequency repeatedly preceded customer failure reports, and built monitoring
   around that signal with no added instrumentation. I want to understand how far such
   early-warning indicators generalize across systems and failure types.
3. **Simulation-based validation before deployment.** I validate robot behavior in Isaac Sim
   and am extending that work to Isaac Lab with domain randomization; I also wrote a multi-robot
   simulator ([mapf-fleet](https://github.com/hurjun/mapf-fleet)) for pre-deployment fleet
   sizing. I am interested in scenario generation and in quantifying what simulation results
   guarantee about field reliability.

---

### Open-Source Projects

> **If you have five minutes:** read [**mapf-fleet**](https://github.com/hurjun/mapf-fleet)
> (a from-scratch multi-robot path-planning engine, benchmarked) and
> [**speculative-decoding-lab**](https://github.com/hurjun/speculative-decoding-lab)
> (LLM inference acceleration, measured against its analytic model).
>
> Every number below is recorded in the linked repository's README, and each repository
> documents how to reproduce or verify it.

#### Multi-robot coordination & monitoring

| Repository | What it is | Evidence |
|---|---|---|
| [**mapf-fleet**](https://github.com/hurjun/mapf-fleet) | Real-time 3D simulation of multi-robot fleets on multi-floor construction sites. A MAPF engine written from scratch in TypeScript — windowed cooperative A\* (WHCA\*) over a space-time reservation table, plus optimal Conflict-Based Search — with capacity-limited elevators and an analytical fleet-size optimizer validated against measured throughput. | **Zero collisions** across **66 seed-swept headless runs / 21,000+ simulation ticks**; CBS matches prioritized planning's throughput at up to **~9×** the compute. |
| [**mlops** · PPE Watchman](https://github.com/hurjun/mlops) | Edge-to-cloud construction-site safety monitoring: YOLOv8 inference on edge clients that stay autonomous offline, lightweight violation events to a FastAPI hub, and live WebSocket fan-out to a Next.js dashboard with bounded-queue backpressure. | **33 passing tests** covering the violation-rule logic and the API hub — event ingestion → persistence → WebSocket fan-out with backpressure. |

#### Sequence models & efficient inference — papers reimplemented from scratch, then measured

| Repository | What it is | Evidence |
|---|---|---|
| [**attention_is_all_you_need**](https://github.com/hurjun/attention_is_all_you_need) | The original Transformer built from `nn.Linear`-level primitives — multi-head attention, masking, the Noam schedule, label smoothing — with cached attention-map visualization. | **98.2%** exact sequence match on a reversal task, reproducible in **~90 s on CPU**; a controlled ablation (identical seeds and initialization) removing positional encoding collapses exact match from **91.2% to 0%** in the ablation configuration. |
| [**xLSTM**](https://github.com/hurjun/xLSTM) | sLSTM and mLSTM cells with exponential gating and stabilized state (Beck et al., NeurIPS 2024); the parallel mLSTM form is unit-tested to match the O(L) recurrence to within **1e-6**. | **100%** accuracy on 64-step recall, where a vanilla LSTM never beats chance (~6.25%) even with up to **2×** the parameters. |
| [**speculative-decoding-lab**](https://github.com/hurjun/speculative-decoding-lab) | Speculative decoding with distribution-preserving acceptance sampling, verified bit-for-bit against greedy decoding, plus draft-length and temperature sweeps compared against the analytic acceptance model. | Up to **1.80× lossless speedup** on Apple Silicon MPS and **0.70× on CPU** — consistent with the memory-bandwidth-bound regime analysis; the analytic tokens-per-round model matches toy-backend measurements within **0.35 token**. |
| [**stock-forecast-benchmark**](https://github.com/hurjun/stock-forecast-benchmark) | Config-driven benchmark of 9 forecasting models (ARIMA, ETS, Prophet, XGBoost, LightGBM, LSTM, GRU, TCN, Transformer) behind one interface, with data-leakage safety enforced by tests and a documented limitations section. | **Prophet ranks first** of the 9 models across MAE, RMSE, and MAPE on 1962–1992 → 1993–2000 held-out data, with an analysis of why the deep models underperform here. |

#### Applied systems

| Repository | What it is | Evidence |
|---|---|---|
| [**stt-nursing-system** · MediVoice](https://github.com/hurjun/stt-nursing-system) | Voice-first nursing documentation: an AI speaker asks assessment questions (TTS), transcribes the answers (STT), and normalizes them into structured records. The working implementation of my undergraduate thesis. | In the thesis evaluation, the assisted workflow cut documentation time for a repeated assessment by **up to 96%**. |

**More:** [**open3d**](https://github.com/hurjun/open3d) — the classic point-cloud/LiDAR pipeline
(RANSAC, DBSCAN, ICP, Poisson meshing) with a headless test suite ·
[**opencv**](https://github.com/hurjun/opencv) — Faster R-CNN person detection with a testable
ROI intrusion-rule engine · [**setpoint**](https://github.com/hurjun/setpoint) — RL fundamentals
(value iteration unit-tested against hand-derived optima, plus REINFORCE) ·
[**futurescole**](https://github.com/hurjun/futurescole) — deterministic, seeded event pipeline
on PostgreSQL + Docker with hermetic tests · [**gre**](https://github.com/hurjun/gre) — adaptive
testing engine evaluated by convergence simulation against a synthetic learner.

---

### Industry Experience

#### 🤖 GoLe Robotics — Full-Stack & Robotics Simulation Engineer · *2026.05 – Present*

Fleet management system (FMS) for autonomous mobile robots on construction sites
([golerobotics.com](https://golerobotics.com)).

- Real-time control and monitoring over the MQTT-based **VDA5050** standard with WebSocket live
  feeds; **PostgreSQL** backend with role-based access control and centralized logging that
  distinguishes network, authentication, and database failures.
- Built an **Isaac Sim** environment where the company's AMR (CAD → URDF) runs its **real ROS2
  nodes unmodified** with Nav2 — validated a complete multi-floor delivery sequence (elevator
  boarding, floor-map switch) end to end before on-site runs. Now extending to **Isaac Lab**
  reinforcement-learning pipelines with domain randomization.

#### 💹 Niflers — Full-Stack Engineer (sole developer) · Fintech · *2024.01 – 2025.11*

Sole owner of frontend, backend, infrastructure, and deployment. Shipped
[CRISK](https://www.crisk.co.kr/), the
[Credit Imbalance Tracker](http://www.enesg.co.kr/), and Credivalue.

- Auto-generated **200,000+** corporate carbon-risk reports; cut report generation from
  **10 minutes to 2** by refactoring a 20,000+ line monolith; daily financial-data pipelines on
  **AWS ECS + Step Functions**.
- Diagnosed and resolved two production incidents — a data-integrity failure during 20-process
  parallel loading, and a framework upgrade that broke every API — experience that shapes how I
  design for data integrity and observability.

#### 🦾 DOGU Robotics — Robot Fleet Control · Web Development Lead · *2022.01 – 2023.12*

Fleet-control platform for **30+ robots across 10+ sites** (hospitals, factories, outdoor) for
clients including Hyundai, SK hynix, and GS EPS.

- Debugged incidents end to end across the control frontend, backend, MQTT broker, and robot ROS
  layers; turned the **MQTT message-frequency anomaly** described under Research Interests into
  proactive monitoring, so engineers responded before customers reported failures.
- Shipped branching diagnostic scripts that field engineers used to localize faults by
  elimination (battery → network → software); WebRTC video streaming, Grafana dashboards, and a
  Vue.js → React migration standardized across 10+ site deployments.

**Earlier:** Mobile Entropy — ERP web services for Incheon City Gas (2021) ·
NSG Co., Ltd. — C++ digital twin of nuclear-plant thermal-hydraulic calculation logic, in
collaboration with K-water (2021).

---

### Education & Awards

- **B.S. in Computer Science & Engineering**, Chungnam National University · *2016.03 – 2025.02*
  — completed while working full-time as a software engineer from 2021 onward.
  Thesis: an AI-speaker nursing-documentation assistant, evaluated in a time-and-motion study —
  [thesis PDF](https://hurjun.github.io/asset/graduation_paper.pdf) ·
  [implementation](https://github.com/hurjun/stt-nursing-system).
- **Grand Prize, KIISE Software Implementation Competition (2017)** — Korean Institute of
  Information Scientists and Engineers, for *Reacord*, a real-time lecture-transcription app
  built and released for deaf and hard-of-hearing classmates.

---

### Technical Skills

<div align="center">

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=Python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=TypeScript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=JavaScript&logoColor=black)
![Java](https://img.shields.io/badge/Java-007396?style=flat&logo=openjdk&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white)

**ML & Robotics**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=PyTorch&logoColor=white)
![ROS](https://img.shields.io/badge/ROS%2FROS2-22314E?style=flat&logo=ros&logoColor=white)
![Isaac Sim](https://img.shields.io/badge/Isaac%20Sim%2FLab-76B900?style=flat&logo=nvidia&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=flat&logo=nvidia&logoColor=white)

**Real-time / Systems**

![MQTT](https://img.shields.io/badge/MQTT-660066?style=flat&logo=MQTT&logoColor=white)
![VDA5050](https://img.shields.io/badge/VDA5050-1F6FEB?style=flat)
![WebSocket](https://img.shields.io/badge/WebSocket-010101?style=flat&logo=socketdotio&logoColor=white)
![WebRTC](https://img.shields.io/badge/WebRTC-333333?style=flat&logo=WebRTC&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white)

**Backend & Frontend**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=FastAPI&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat&logo=SpringBoot&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-5FA04E?style=flat&logo=nodedotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=React&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=Next.js&logoColor=white)

**Cloud, Infra & Data**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=AmazonWebServices&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=Docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat&logo=nginx&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=MySQL&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=Redis&logoColor=white)

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=100&section=footer" />

</div>
