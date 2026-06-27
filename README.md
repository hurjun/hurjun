<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=180&section=header&text=Heojun%20Hur&fontSize=64&fontAlignY=36&desc=Robotics%20%26%20ML%20Engineer&descAlignY=58&descSize=22" />
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

I build and operate real robotic and ML systems. Over ~4 years in industry I led the
real-time monitoring and control platform for a fleet of **30+ autonomous service robots**
(WebRTC telemetry, MQTT command channels) deployed across hospital, factory, and outdoor
environments, and shipped data-intensive backends end to end. That production work pulled me
toward the research questions underneath it — **how fleets of robots coordinate, perceive, and
plan at scale** — which is why I'm now pursuing graduate study. The repositories below are my
own from-scratch reimplementations of core algorithms and reproducible engineering systems,
built to understand the methods rather than wrap a library.

---

### Research Interests

I am drawn to the algorithms that let many agents **coordinate, perceive, and plan at scale**,
and to the **ML systems** that make those algorithms run efficiently and verifiably. My
self-directed work clusters into four threads:

- **Multi-robot coordination & multi-agent path finding (MAPF)** — collision-free planning,
  conflict-based search, fleet-size and throughput optimization.
- **Efficient ML & sequence modeling** — attention/recurrent architectures and inference
  acceleration, re-derived from the papers and measured, not wrapped.
- **Perception & 3D** — edge vision pipelines and point-cloud/LiDAR processing that turn raw
  sensor data into reliable real-time signals.
- **Applied full-stack & systems** — taking a research idea all the way to a tested,
  reproducible, deployable system.

---

### Selected Projects

Every project below is an inspectable repository with code, tests, CI, and a reproducible
**headline result** — each number is quoted directly from that repo's own README and figures.

#### Efficient ML & Sequence Modeling

| Project | What it is | Headline result |
|---|---|---|
| [**attention_is_all_you_need**](https://github.com/hurjun/attention_is_all_you_need) | From-scratch PyTorch **Transformer** (Vaswani et al., 2017) — scaled-dot-product / multi-head attention, sinusoidal encodings, Noam warmup, label smoothing. | **98.2%** greedy exact-match on a synthetic reverse task with a ~0.66 M-param model, fully reproducible in ~90 s on CPU. |
| [**xLSTM**](https://github.com/hurjun/xLSTM) | From-scratch reimplementation of xLSTM's **sLSTM / mLSTM** cells (exponential gating, matrix memory, stabilizer state) — NeurIPS 2024. | **100%** accuracy on 64-step recall, where a vanilla LSTM stays at chance (~6.5%) even given **2× the parameters** — an 8× longer reliable horizon. |
| [**speculative-decoding-lab**](https://github.com/hurjun/speculative-decoding-lab) | From-scratch **speculative decoding** with distribution-preserving acceptance sampling, unit-tested for exact-distribution correctness. | **Up to 1.80×** lossless speedup (gpt2-large + distilgpt2 draft, MPS), output token-for-token identical to autoregressive decoding; acceptance rate α tracks draft/target similarity. |
| [**stock-forecast-benchmark**](https://github.com/hurjun/stock-forecast-benchmark) | Config-driven, **leakage-aware** benchmark of 9 forecasters (ARIMA → Transformer) behind one `BaseForecaster` interface, with an auto-generated leaderboard. | Across 30 yrs train / 8 yrs held-out test (3 tickers), **Prophet leads** (MAE 117.45) over LSTM, GRU, XGBoost and a Transformer — apples-to-apples. |

#### Multi-Robot Coordination & Robotics

| Project | What it is | Headline result |
|---|---|---|
| [**mapf-fleet**](https://github.com/hurjun/mapf-fleet) &nbsp;⭐ *flagship* | Interactive 3D simulator of a multi-robot construction-site fleet on a **from-scratch TypeScript MAPF engine** — cooperative windowed space-time A\* (WHCA\*), optimal **Conflict-Based Search (CBS)**, capacity-limited elevators, analytical fleet-size optimizer. | **Zero collisions across all 66 seed-swept benchmark runs (21,000+ simulated ticks)**; throughput scales to 9.3 deliveries/min at 16 agents, with the optimizer's predicted bottleneck validated live against the running sim. |
| [**setpoint**](https://github.com/hurjun/setpoint) | **Reinforcement learning from scratch** (NumPy/PyTorch) for HVAC setpoint control as an MDP — value iteration and REINFORCE, each unit-tested against problems with known answers. | Value iteration converges to the hand-derived optimum `V*=[7,10,7]`; REINFORCE improves mean episode return from **−112.7 → −34.7** over 400 episodes. |

#### Perception & 3D

| Project | What it is | Headline result |
|---|---|---|
| [**mlops** · PPE Watchman](https://github.com/hurjun/mlops) | Edge-to-cloud industrial-safety perception: a YOLOv8 edge detector streams lightweight violation **events** to a FastAPI hub that persists them and broadcasts over **WebSocket** to a live Next.js dashboard. | Offline-first distributed event pipeline (edge inference → central aggregation → live browser), locked down by **33 passing tests** (8 rules + 25 API/broadcaster) and CI. |
| [**open3d**](https://github.com/hurjun/open3d) | A **7-stage** tour of the classic 3D point-cloud / LiDAR pipeline — voxel filtering, PCA normals, RANSAC ground segmentation, DBSCAN clustering, ICP registration, Poisson reconstruction, mesh validation, `.las` I/O. | Each stage is a runnable script that prints quantitative metrics (ICP `fitness` / `inlier_rmse`, RANSAC inliers, cluster counts) and renders a figure — the building blocks under SLAM and mapping. |
| [**opencv**](https://github.com/hurjun/opencv) | OpenCV preprocessing + a torchvision **Faster R-CNN** person detector + an ROI intrusion rule engine + MOG2 motion detection, wired into one `video → detect → rule → log` driver. | Real detection (single person at score **0.999** on the test image); the non-detection path runs at **~270 FPS** on CPU, with append-only CSV event logging. |

#### Applied Full-Stack & Systems

| Project | What it is | Headline result |
|---|---|---|
| [**stt-nursing-system** · MediVoice](https://github.com/hurjun/stt-nursing-system) | Voice-first nursing-documentation app (React/TypeScript) that turns bedside TTS/STT rounds into structured EMR-style records — a deployed realization of my **undergraduate research**. | In that study the assisted workflow cut documentation time by **up to 96%** and Google's Korean speech engine hit a **0% character error rate** on the reference utterance — both reproduced in-app. |
| [**gre**](https://github.com/hurjun/gre) | Full-stack **adaptive** GRE practice platform (FastAPI + React + MySQL): serves one question at a time, steps difficulty up on a correct answer and down on a miss, retires solved questions. | A static question bank turned into a personalized per-section study loop; screenshots are real renders of the running app. |
| [**dfinite** · FitFlow](https://github.com/hurjun/dfinite) | FastAPI + PostgreSQL back-office for a fictional fitness chain — the focus is **correctness engineering** on a working-but-buggy proof of concept. | **5 subtle business-logic defects** diagnosed to root cause, fixed, and locked down with a regression suite that runs with no external DB (isolated SQLite) plus lint + CI. |
| [**futurescole**](https://github.com/hurjun/futurescole) | Containerized **data pipeline** (Python + PostgreSQL + Docker Compose) that synthesizes realistic web-service telemetry, stores it with a deliberate schema, and renders analytics charts. | A reproducible batch pipeline modeling session funnels, conversion/error rates and peak-hour bias the way a real e-commerce backend produces them. |

---

### Technical Skills

<div align="center">

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=Python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=TypeScript&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=JavaScript&logoColor=black)

**ML / Robotics**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=PyTorch&logoColor=white)
![Ultralytics YOLO](https://img.shields.io/badge/YOLOv8-111F68?style=flat&logo=ultralytics&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![WebRTC](https://img.shields.io/badge/WebRTC-333333?style=flat&logo=WebRTC&logoColor=white)
![MQTT](https://img.shields.io/badge/MQTT-660066?style=flat&logo=MQTT&logoColor=white)

**Systems / Web / Infra**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=FastAPI&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat&logo=SpringBoot&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=React&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=Next.js&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=Docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=AmazonWebServices&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=MySQL&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=Redis&logoColor=white)

</div>

---

### Industry Experience

```
Jan 2022 – Dec 2023   Robot Control Dev & Web Lead   Dogugonggan
                      Real-time monitoring & control for 30+ autonomous robots across
                      hospital, factory, and outdoor sites — WebRTC telemetry, MQTT
                      commands, voice (TTS/STT) interface.

Jan 2024 – Present    Full-Stack Developer            Niflers (Fintech)
                      Climate-risk reporting platform generating 200K+ corporate reports;
                      AWS data pipelines (ECS, Step Functions, Lambda) with FastAPI backends.

2021                  Full-Stack / Freelance          Mobile Entropy · NSG
```

---

<div align="center">

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=hurjun&layout=compact&hide_border=true" />
&nbsp;
<img src="https://github-readme-stats.vercel.app/api?username=hurjun&show_icons=true&hide_border=true" />

<br><br>

[![Solved.ac Profile](http://mazassumnida.wtf/api/v2/generate_badge?boj=hurjun96)](https://solved.ac/hurjun96)

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=100&section=footer" />

</div>
