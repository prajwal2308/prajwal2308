```
██████╗ ██████╗  █████╗      ██╗██╗    ██╗ █████╗ ██╗
██╔══██╗██╔══██╗██╔══██╗     ██║██║    ██║██╔══██╗██║
██████╔╝██████╔╝███████║     ██║██║ █╗ ██║███████║██║
██╔═══╝ ██╔══██╗██╔══██║██   ██║██║███╗██║██╔══██║██║
██║     ██║  ██║██║  ██║╚█████╔╝╚███╔███╔╝██║  ██║███████╗
╚═╝     ╚═╝  ╚═╝╚═╝  ╚═╝ ╚════╝  ╚══╝╚══╝ ╚═╝  ╚═╝╚══════╝
        S O F T W A R E   ·   C L O U D   ·   A I
```

> **Prajwal Srinivas** — MS Computer Science, Rutgers University
> United States · open to relocation · open to work
> **[prajwal2308.github.io](https://prajwal2308.github.io)** · [LinkedIn](https://linkedin.com/in/prajwalsrinivas238) · [prajwal.srinivas238@gmail.com](mailto:prajwal.srinivas238@gmail.com)

---

## What I actually do

Almost everything I build sits **between two systems that don't trust each other yet**.

```
      your app                  the layer I build                  the world
   ┌─────────────┐          ┌───────────────────────┐          ┌─────────────┐
   │             │          │  guardrail → route    │          │  6 model    │
   │  requests   │─────────▶│  telemetry  → retry   │─────────▶│  providers  │
   │             │          │  failover   → redact  │          │             │
   └─────────────┘          └───────────┬───────────┘          └─────────────┘
                                        │
                                   when a tier dies,
                              the caller never finds out
```

A gateway between an application and six LLM providers. A governance harness
between a coding agent and the tools it wants to call. A planner between a vague
goal and a pool of workers. Cloudflare failover between a region that's up and one
that isn't. That middle layer is where the interesting engineering lives, because
it's where you find out what actually breaks.

I'm not precious about which part of the stack. In the last year I shipped a
**native macOS app in Swift**, an **LLM gateway on Kubernetes**, and a **Next.js
product across AWS and GCP**.

---

## Selected work

<table>
<tr><td width="180"><strong>VACS</strong><br><sub>Aug 2026 · Swift</sub></td>
<td>A native macOS disk cleaner for developers — the one audience for whom <em>"junk files"</em> is the wrong abstraction. Xcode DerivedData, the Docker VM disk, Ollama weights and Playwright browsers all look identical to a generic cleaner. VACS names all <strong>96 audited paths</strong> in plain English and gives the correct way to reclaim each, which is often <em>not</em> deleting the folder. Trash-only by default; nothing anywhere asks for <code>sudo</code>.<br>
<a href="https://prajwal2308.github.io/VACS/">website</a> · <a href="https://github.com/prajwal2308/VACS">source</a> · <a href="https://github.com/prajwal2308/VACS/releases">download</a></td></tr>

<tr><td><strong>LLMOps<br>Control Plane</strong><br><sub>Aug 2026 · live</sub></td>
<td>A self-hostable gateway to OpenAI, Anthropic, Gemini, Bedrock, Fireworks and xAI behind one <strong>OpenAI-compatible API</strong> — adoption is a base-URL change, not a rewrite. Complexity-based routing, automatic failover chains, prompt-injection defense inbound, PII redaction outbound, and per-request latency/token/cost telemetry on a live SSE dashboard. Stateless and horizontally scalable; ships as Docker, Helm and Terraform.<br>
<a href="https://llmops-control-plane.onrender.com">live dashboard</a> · <a href="https://github.com/prajwal2308/LLMOps-Control-Plane">source</a></td></tr>

<tr><td><strong>SAGE</strong><br><sub>May 2026 · 1st place</sub></td>
<td><strong>Winner, AESIA × UN Tech Over Hackathon.</strong> An open-source governance harness for AI coding agents — Claude Code, Cursor, OpenCode, Cline — that evaluates what an agent is about to do <em>before</em> it happens, not in a log you read the next morning. Hooks the Model Context Protocol boundary, so one integration covers every agent. Prompt-risk scoring, EU AI Act compliance path, cryptographic audit logs.<br>
<a href="https://www.npmjs.com/package/sage-governance">npm</a> · <a href="https://github.com/Olustar/supervisory-agentic-governance-engine">source</a></td></tr>

<tr><td><strong>Hyper-<br>Orchestrator</strong><br><sub>Apr 2026 · 4.2×</sub></td>
<td>A Planner Agent decomposes a goal and resolves the dependency DAG <em>before</em> any worker starts; adaptive pools then run independent branches simultaneously and a fusion pass merges the results. <strong>4.2× faster than sequential execution</strong> on identical workloads. Deliberately single-file and dependency-light — the point was to understand the primitive, not wrap someone else's.<br>
<a href="https://github.com/prajwal2308/hyper-orchestrator">source</a></td></tr>

<tr><td><strong>Thinker–<br>Curator</strong><br><sub>Jan 2026 · research</sub></td>
<td>Graduate research on LLM long-term memory. A <strong>Thinker</strong> proposes salient facts as a conversation happens; a <strong>Curator</strong> scores what gets admitted. Curation happens <em>before</em> the context window fills rather than reactively at query time — which is where multi-hop retrieval precision comes from.<br>
<a href="https://github.com/prajwal2308/Proactive_Retrieval_Thinker_Curator_Model_for_AI_Memory">source</a></td></tr>
</table>

<details>
<summary><strong>More on GitHub</strong></summary>
<br>

- **[Cloud Microservices Platform](https://github.com/prajwal2308/cloud-microservices-platform)** — Node gateway, Go auth and Python data services on EKS, provisioned end to end in Terraform with ALB, RDS replicas, ElastiCache, Prometheus and Grafana.
- **[Real-time AI Analytics](https://github.com/prajwal2308/realtime-ai-analytics)** — Streaming ingest with ML anomaly detection, WebSocket live feed, TimescaleDB persistence.
- **[LoRaWAN Mesh Simulator](https://github.com/prajwal2308/DIS_Final_Project_LoRAWAN)** — Four containerised multi-hop UDP mesh implementations benchmarked under fault injection.

</details>

---

## Track record

```
 99.9%   uptime on the platform I run          1k+ users, AWS + GCP, Cloudflare failover
  4.2×   orchestration speedup                 measured against sequential execution
   95%   test coverage in a 4-week contract    serverless GCP, 100% on-time MVP
   20%   drop in post-release defects          agent desktop for global telecom carriers
  200+   students taught                       web technologies and SQL, Rutgers
   1st   AESIA × UN Tech Over Hackathon        out of the full field
```

---

## Experience

```
2026 ─┬─ Beunec Technologies · Cloud & Systems Engineer, Team Lead      May 2025 → now
      │    Beunec Cloud: Next.js + two distributed backends across AWS and GCP,
      │    1k+ users at 99.9% availability. Global load balancing and automated
      │    multi-region failover via Cloudflare. Redis in front of MongoDB to kill
      │    a session-read bottleneck. Aselius AI: GenAI engine, E2E encrypted, GDPR.
      │
      ├─ Universal Selfcare · Cloud Systems Engineer & Project Lead  Dec 2025 → Jan 2026
      │    Serverless GCP backend (Cloud Functions, Cloud Run, GKE) at 95% test
      │    coverage in four weeks. Led five developers to a 100% on-time MVP.
      │
      ├─ Rutgers University · Graduate Teaching Assistant           Sept 2024 → May 2026
      │    200+ students in web technologies and SQL. Code review, live debugging.
      │
2023 ─┴─ CSG International · Software Developer                      Feb 2023 → Aug 2024
           Customer Connect, the agent desktop used by global telecom carriers.
           Cut post-release defect rates 20% via test coverage and release review.
```

---

## Toolkit

| | |
|---|---|
| **Languages** | Python · TypeScript · JavaScript · Go · Swift · Java · SQL · Bash |
| **Cloud & DevOps** | AWS · GCP · Kubernetes (EKS/GKE) · Helm · Docker · Terraform · Cloudflare · GitHub Actions · CI/CD |
| **AI & data** | LangChain · MCP · RAG & vector search · PyTorch · OpenAI & Anthropic APIs · PostgreSQL · MongoDB · Redis · Kafka |
| **Product & frontend** | Next.js · React · Node/Express · FastAPI · Flask · SwiftUI · Tailwind · REST · gRPC |
| **Systems** | Distributed systems · system design · microservices · load balancing & failover · OpenTelemetry · Prometheus & Grafana |

---

## Education

| | | |
|---|---|---|
| **MS Computer Science** | Rutgers University–New Brunswick | GPA 3.71/4.0 · May 2026 |
| **BE Computer Science** | MVJ College of Engineering | GPA 9.1/10 · May 2023 |
| **Certifications** | AWS Cloud Practitioner · Salesforce Developer Catalyst | |

---

```
$ whoami
prajwal — open to software, platform, cloud/DevOps and AI engineering roles.
          United States, ready to relocate. F-1 OPT, STEM extension eligible.

$ contact
prajwal.srinivas238@gmail.com
```
