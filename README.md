<div align="center">

# Hi, I'm Minjoo Kim 👋

### Backend & Infrastructure Engineer

Ewha Womans University, Computer Science · Class of 2027

<br/>

[![Blog](https://img.shields.io/badge/Tech%20Blog-Tistory-FF5A4A?style=flat-square)](https://blogger8342.tistory.com/)
[![Email](https://img.shields.io/badge/Email-Contact-333333?style=flat-square&logo=gmail&logoColor=white)](mailto:이메일주소입력)

</div>

---

## About Me

I am a backend-oriented software engineering student who builds services and the infrastructure they run on.

I code AWS infrastructure with Terraform, automate deployments without storing long-lived credentials, and measure system limits before tuning them.  
My focus is on making failures visible — a deployment that reports success while the application returns 500 is the kind of problem I keep working against.

<br/>

| | |
| --- | --- |
| 🔭 Currently working on | **Pally** — AI English conversation app |
| 🌱 Currently learning | Distributed Systems, Load Testing, Observability Design |
| 💼 Recent experience | R&D Internship at **Xenon** — AI Agent Product Benchmarking |
| 🎓 Education | Ewha Womans University, Computer Science |
| 📝 Blog | [blogger8342.tistory.com](https://blogger8342.tistory.com/) |

---

## Tech Stack

### Cloud & DevOps

![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)

### Observability & Testing

![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![Loki](https://img.shields.io/badge/Loki-F46800?style=flat-square&logo=grafana&logoColor=white)
![k6](https://img.shields.io/badge/k6-7D64FF?style=flat-square&logo=k6&logoColor=white)

### Backend

![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)

### Frontend

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=flat-square&logo=react&logoColor=black)

---

## Featured Projects

---

### ☁️ Jobai

> AI-based Job Posting Monitoring Platform  
> `2026.05 – 2026.09` · 9-person team

**Role**  
Backend & Infrastructure Engineer · Sole Infrastructure Owner

**Tech**  
AWS · Terraform · GitHub Actions · Spring Boot · PostgreSQL · Redis · Prometheus · Grafana · Loki · k6

**Highlights**

- Codified **67 AWS resources** with Terraform, including VPC, EC2, RDS, S3, ECR, IAM, and SSM.
- Migrated deployment from SSH to **AWS SSM**, and from access keys to **GitHub Actions OIDC**.
- Built an observability stack with Prometheus, Grafana, and Loki, plus **7 Slack alert rules** based on measured data.
- Reproduced a connection pool exhaustion issue with k6: **15 concurrent resume uploads** caused an **87.3% failure rate** on an unrelated search API.
- Resized the instance based on measurements: swap usage **871MB → 0**, available memory **5.9% → 37.5%**.
- Added **3-stage deployment verification with automatic rollback** after a release succeeded while uploads returned 500.
- Documented **14 ADRs**, an incident postmortem, a runbook, and a cost analysis identifying **$108/month** post-free-tier exposure.

---

### 🔬 Xenon R&D Internship

> AI Agent Product Benchmarking & Issue Resolution  
> `2026.06 – 2026.08` · 8 weeks

**Role**  
R&D Intern · Advanced Development Team

**Tech**  
Terminal-Bench 2.0 · Harbor · MCP · Docker · Python · TypeScript

**Highlights**

- Extracted the company’s agent CLI into a standalone build and wrote a **Harbor adapter** to evaluate the product itself across **89 benchmark tasks**.
- Measured a **12%p performance gap** against the standard harness, reproduced across two different models.
- Traced **73 of 267 failures** to two confirmed source-level bugs: missing timeout handling and unhandled EPIPE on stdin.
- After fixes, agent-level errors dropped from **32% to 10.5%**, and crash-type failures fell from **24 to 3**.
- Revised the reporting standard to separate **infrastructure failures** from **model failures**, preventing model performance from being underreported.
- Designed a TypeScript-based PPTX generation MCP for **air-gapped environments**, including WCAG contrast and text overflow validation criteria.

---

### 🎙️ Pally

> AI English Conversation App  
> `2026.03 – Present` · Capstone Project

**Role**  
Backend Engineer · Sole Backend Owner after MVP

**Tech**  
FastAPI · Supabase · PostgreSQL · Auth · RLS · Pydantic · GitHub Actions

**Highlights**

- Implemented **atomic quota deduction** using `INSERT .. ON CONFLICT DO UPDATE` row locking.
- Audited **6 bypass scenarios** and kept quota RPCs as INVOKER instead of `SECURITY DEFINER`.
- Designed RLS with **no client-side write policies** for quota, achievements, and subscription entitlement.
- Verified the security model with **19/19 security tests**.
- Built a swappable AI engine interface with **3-tier fallback**.
- Designed an `(items, failed)` contract to distinguish “no correction needed” from “generation failed”.
- Recovered **167 lines** of API code removed by a stale-base merge and added a CI route presence check.

---

### 🚇 WeatherTago

> Weather-based Subway Congestion Prediction App  
> `2025.06 – 2025.07` · TAVE 15th · 9-person team

**Role**  
Frontend Developer · React Native

**Tech**  
React Native · Expo · TypeScript · Axios · Context API · Fuse.js

**Highlights**

- Built the congestion, facility, notice, and home screens, contributing **131 commits** out of 308.
- Generated direction buttons dynamically from server response keys, supporting Line 2’s inner/outer loop and other lines’ up/down directions.
- Normalized transfer stations returning multiple records into a single representative entry by minimum `stationId`.
- Handled public APIs returning **XML error bodies instead of JSON**, preventing app crashes during upstream outages.
- Absorbed a mid-development backend contract change through a **Context-based name-to-ID resolution layer**.

---

<div align="center">

### Thanks for visiting 🌱

[![Tistory](https://github-readme-tistory-card.vercel.app/api/badge?name=Tistory)](https://blogger8342.tistory.com/)

</div>
