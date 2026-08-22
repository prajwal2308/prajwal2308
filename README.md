<h1 align="center">Prajwal Srinivas</h1>

<p align="center">
  <strong>Software · Cloud &amp; DevOps · AI Engineering</strong><br>
  MS Computer Science, Rutgers University · United States, open to relocation
</p>

<p align="center">
  <a href="https://prajwal2308.github.io"><strong>Portfolio</strong></a> ·
  <a href="https://linkedin.com/in/prajwalsrinivas238">LinkedIn</a> ·
  <a href="mailto:prajwal.srinivas238@gmail.com">Email</a>
</p>

---

I build the layer most teams end up rewriting badly: gateways, control planes and
orchestrators that keep systems observable, routable and standing up when a
dependency isn't. I'm not precious about which part of the stack — in the last year
I shipped a native macOS app in Swift, an LLM gateway on Kubernetes, and a Next.js
product across AWS and GCP.

**Currently:** Cloud &amp; Systems Engineer and Team Lead at Beunec Technologies.
**Open to** software, platform, cloud/DevOps and AI engineering roles.

---

## Selected work

### [VACS](https://github.com/prajwal2308/VACS) · [website](https://prajwal2308.github.io/VACS/)
`Swift` `SwiftUI` `macOS 14+`

A native macOS disk cleaner built for developers — the one audience for whom
"junk files" is the wrong abstraction. Xcode DerivedData, the Docker VM disk,
Ollama weights and Playwright browsers all look identical to a generic cleaner.
VACS names all 96 audited paths in plain English and gives you the correct way to
reclaim each one, which is often not deleting the folder. Trash-only by default,
zero telemetry, and no step anywhere asks for `sudo`.

### [LLMOps Control Plane](https://github.com/prajwal2308/LLMOps-Control-Plane) · [live dashboard](https://llmops-control-plane.onrender.com)
`FastAPI` `Kubernetes` `Helm` `Terraform` `OpenTelemetry`

A self-hostable gateway between your applications and OpenAI, Anthropic, Gemini,
Bedrock, Fireworks and xAI, speaking an OpenAI-compatible API so adoption is a
base-URL change rather than a rewrite. Complexity-based model routing with
automatic failover chains across provider tiers, prompt-injection defense inbound
and PII redaction outbound, and per-request latency/token/cost telemetry streamed
to a live SSE dashboard. Stateless and horizontally scalable; ships as Docker, a
Helm chart and Terraform.

### SAGE — Supervisory Agentic Governance Engine 🏆
`MCP` `TypeScript` `AI governance`
[npm](https://www.npmjs.com/package/sage-governance) ·
[source](https://github.com/Olustar/supervisory-agentic-governance-engine)

**1st place, AESIA × UN Tech Over Hackathon.** An open-source governance harness
for AI coding agents (Claude Code, Cursor, OpenCode, Cline) that evaluates what an
agent is about to do *before* it happens, rather than auditing it afterwards. Hooks
the Model Context Protocol boundary — one integration covers every agent — with
prompt-risk scoring, an EU AI Act compliance path and cryptographic audit logs.

### [Hyper-Orchestrator](https://github.com/prajwal2308/hyper-orchestrator)
`Python` `AsyncIO` `DAG scheduling`

A parallel execution engine where a Planner Agent decomposes a high-level goal and
resolves the dependency DAG before any worker starts, then adaptive worker pools
run the independent branches simultaneously. **4.2× faster than sequential
execution** on the same workloads. Deliberately single-file and dependency-light —
the point was to understand the primitive, not wrap someone else's.

### [Thinker–Curator](https://github.com/prajwal2308/Proactive_Retrieval_Thinker_Curator_Model_for_AI_Memory)
`Python` `LangChain` `RAG` `PyTorch`

Graduate research on LLM long-term memory. A **Thinker** proposes salient facts as a
conversation happens and a **Curator** scores what gets admitted — curating *before*
the context window fills instead of retrieving reactively at query time. Improves
retrieval precision on multi-hop queries.

<details>
<summary><strong>More on GitHub</strong></summary>

- **[Cloud Microservices Platform](https://github.com/prajwal2308/cloud-microservices-platform)** — Node gateway, Go auth and Python data services on EKS, provisioned end to end in Terraform with ALB, RDS replicas, ElastiCache, Prometheus and Grafana.
- **[Real-time AI Analytics](https://github.com/prajwal2308/realtime-ai-analytics)** — Streaming ingest with ML anomaly detection, WebSocket live feed and TimescaleDB persistence.
- **[LoRaWAN Mesh Simulator](https://github.com/prajwal2308/DIS_Final_Project_LoRAWAN)** — Four containerised multi-hop UDP mesh implementations benchmarked under fault injection.

</details>

---

## Experience

| | | |
|---|---|---|
| **Beunec Technologies** | Cloud &amp; Systems Engineer, Team Lead | May 2025 – Present |
| **Universal Selfcare** | Cloud Systems Engineer &amp; Project Lead | Dec 2025 – Jan 2026 |
| **Rutgers University** | Graduate Teaching Assistant | Sept 2024 – May 2026 |
| **CSG International** | Software Developer | Feb 2023 – Aug 2024 |

At **Beunec** I architected Beunec Cloud — a Next.js frontend and two distributed
backend microservices across AWS and GCP — serving 1k+ users at 99.9% availability,
with global load balancing and automated multi-region failover via Cloudflare, and
a Redis layer in front of MongoDB that removed a session-read bottleneck.
At **Universal Selfcare** I delivered a serverless GCP backend (Cloud Functions,
Cloud Run, GKE) at 95% test coverage in a four-week contract, coordinating five
developers to a 100% on-time MVP. At **Rutgers** I taught 200+ students web
technologies and SQL. At **CSG** I shipped features for Customer Connect, the agent
desktop used by global telecom carriers, cutting post-release defects 20%.

---

## Toolkit

**Languages** Python · TypeScript · JavaScript · Go · Swift · Java · SQL · Bash

**Cloud &amp; DevOps** AWS · GCP · Kubernetes (EKS/GKE) · Helm · Docker · Terraform · Cloudflare · GitHub Actions · CI/CD

**AI &amp; data** LangChain · MCP · RAG &amp; vector search · PyTorch · OpenAI &amp; Anthropic APIs · PostgreSQL · MongoDB · Redis · Kafka

**Product &amp; frontend** Next.js · React · Node/Express · FastAPI · Flask · SwiftUI · Tailwind · REST · gRPC

**Systems** Distributed systems · system design · microservices · load balancing &amp; failover · OpenTelemetry · Prometheus &amp; Grafana

---

## Education

**MS Computer Science** — Rutgers University–New Brunswick, GPA 3.71/4.0 · May 2026
**BE Computer Science** — MVJ College of Engineering, GPA 9.1/10 · May 2023
**Certifications** — AWS Cloud Practitioner · Salesforce Developer Catalyst

---

<p align="center"><em>Open to new opportunities — <a href="mailto:prajwal.srinivas238@gmail.com">get in touch</a>.</em></p>
