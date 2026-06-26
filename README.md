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

- **Multi-robot coordination & multi-agent path finding (MAPF)** — collision-free planning,
  conflict-based search, fleet-size and throughput optimization.
- **Perception for robotics** — edge vision pipelines and the systems that turn detection
  models into reliable real-time signals.
- **ML systems & sequence modeling** — efficient inference, and recurrent/attention
  architectures studied at the implementation level.

---

### Selected Projects

Each links to an inspectable repository with code, tests, and reported results.

| Project | What it is — and why it matters |
|---|---|
| [**mapf-fleet**](https://github.com/hurjun/mapf-fleet) | Interactive 3D simulator of a multi-robot construction-site fleet, powered by a **from-scratch TypeScript MAPF engine** — cooperative windowed space-time A\* (WHCA\*), optimal **Conflict-Based Search (CBS)**, capacity-limited elevators, and an analytical fleet-size optimizer. *My flagship robotics-coordination project.* |
| [**mlops** · PPE Watchman](https://github.com/hurjun/mlops) | Edge-to-cloud industrial-safety perception: a YOLOv8 edge detector streams lightweight violation **events** to a FastAPI hub that persists them and broadcasts over **WebSocket** to a live Next.js operator dashboard. *The edge-inference + central-aggregation pattern behind real robot/perception fleets.* |
| [**xLSTM**](https://github.com/hurjun/xLSTM) | From-scratch PyTorch reimplementation of xLSTM's **sLSTM/mLSTM** cells (exponential gating, matrix memory, stabilizer state). On a 64-step recall task it reaches **100%** accuracy where a vanilla LSTM never beats chance. *Implementing a 2024 sequence architecture from the paper up.* |
| [**attention_is_all_you_need**](https://github.com/hurjun/attention_is_all_you_need) | From-scratch PyTorch **Transformer** (Vaswani et al., 2017) — scaled dot-product/multi-head attention, sinusoidal positional encoding, Noam warmup schedule, label smoothing — trained to **~98%** exact-match on a CPU-reproducible task. *Attention understood at the implementation level.* |
| [**stock-forecast-benchmark**](https://github.com/hurjun/stock-forecast-benchmark) | Config-driven, **leakage-aware** benchmark of 9 forecasting models (ARIMA → Transformer) behind one `BaseForecaster` interface, with an auto-generated leaderboard. *Rigorous, apples-to-apples experimental methodology.* |
| [**stt-nursing-system**](https://github.com/hurjun/stt-nursing-system) | Voice-first nursing-documentation app (React/TypeScript) that turns simulated bedside TTS/STT rounds into structured EMR-style records — a working realization of my **undergraduate research**. *Carrying a research idea through to a deployed system.* |
| [**speculative-decoding-lab**](https://github.com/hurjun/speculative-decoding-lab) | Research notes synthesizing speculative decoding and quantization into one testable question: how draft-model precision trades off against acceptance rate. *Reading SOTA ML-systems papers critically.* (notes, work in progress) |

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
