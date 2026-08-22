```console
$ kubectl get engineer prajwal -o wide

NAME      DISCIPLINES                        LOCATION        STATUS   OPEN TO WORK
prajwal   software · cloud/devops · ai       United States   Ready    true
          MS Computer Science, Rutgers       will relocate            F-1 OPT (STEM)
```

**[prajwal2308.github.io](https://prajwal2308.github.io)** · [LinkedIn](https://linkedin.com/in/prajwalsrinivas238) · [prajwal.srinivas238@gmail.com](mailto:prajwal.srinivas238@gmail.com)

---

## The through-line

Almost everything I build sits **between two systems that don't trust each other yet.**

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

A gateway between an app and six LLM providers. A governance harness between a
coding agent and the tools it wants to call. A planner between a vague goal and a
pool of workers. Cloudflare failover between a region that's up and one that isn't.
That middle layer is where the interesting engineering lives — it's where you find
out what actually breaks.

I'm not precious about which part of the stack, either. In the last year I shipped a
**native macOS app in Swift**, an **LLM gateway on Kubernetes**, and a **Next.js
product across AWS and GCP**.

---

## Deployments

```console
$ kubectl get deployments -n portfolio --sort-by=.metadata.creationTimestamp

NAME                   STACK                              STATUS      READY   AGE
llmops-control-plane   fastapi · k8s · helm · terraform   Running      1/1    Aug 2026
vacs                   swift · swiftui · macos            Released     1/1    Aug 2026
sage-governance        mcp · typescript                   Published    1/1    May 2026
hyper-orchestrator     python · asyncio                   Benchmarked  1/1    Apr 2026
thinker-curator        langchain · rag · pytorch          Research     1/1    Jan 2026
```

<table>
<tr><td width="170"><strong>LLMOps<br>Control Plane</strong><br><sub>live in production</sub></td>
<td>A self-hostable gateway to OpenAI, Anthropic, Gemini, Bedrock, Fireworks and xAI behind one <strong>OpenAI-compatible API</strong> — adoption is a base-URL change, not a rewrite. Complexity-based routing sends cheap prompts to cheap models; when a provider errors, an automatic failover chain walks the tiers and the client sees one slightly slower success instead of a 500. Prompt-injection defense inbound, PII redaction outbound, per-request latency/token/cost telemetry on a live SSE dashboard.<br>
<a href="https://llmops-control-plane.onrender.com">live dashboard</a> · <a href="https://github.com/prajwal2308/LLMOps-Control-Plane">source</a></td></tr>

<tr><td><strong>VACS</strong><br><sub>native macOS app</sub></td>
<td>A disk cleaner for developers — the one audience for whom <em>"junk files"</em> is the wrong abstraction. Xcode DerivedData, the Docker VM disk, Ollama weights and Playwright browsers all look identical to a generic cleaner. VACS names all <strong>96 audited paths</strong> in plain English and gives the correct way to reclaim each, which is often <em>not</em> deleting the folder. For a live Docker VM it copies <code>docker system prune -a</code> instead of offering a delete button. Trash-only by default; nothing anywhere asks for <code>sudo</code>.<br>
<a href="https://prajwal2308.github.io/VACS/">website</a> · <a href="https://github.com/prajwal2308/VACS">source</a> · <a href="https://github.com/prajwal2308/VACS/releases">download</a></td></tr>

<tr><td><strong>SAGE</strong><br><sub>1st place — AESIA × UN</sub></td>
<td>Coding agents now write files, run shell commands and call APIs on their own. The industry's answer has mostly been a log you read afterwards — <strong>and a log is not a control.</strong> SAGE is an open-source governance harness for Claude Code, Cursor, OpenCode and Cline that evaluates what an agent is about to do <em>before</em> it happens. It hooks the Model Context Protocol boundary, the one place every tool call has to pass through, so one integration covers all of them. Prompt-risk scoring, EU AI Act compliance path, cryptographic audit logs.<br>
<a href="https://www.npmjs.com/package/sage-governance">npm</a> · <a href="https://github.com/Olustar/supervisory-agentic-governance-engine">source</a></td></tr>

<tr><td><strong>Hyper-<br>Orchestrator</strong><br><sub>4.2× speedup</sub></td>
<td>Most agent workflows run one step at a time because that's the easy thing to write — even when four of the six steps have nothing to do with each other. A Planner Agent decomposes the goal and resolves the dependency DAG <em>before</em> any worker starts, then adaptive pools run the independent branches simultaneously and a fusion pass merges the results. Deliberately single-file and dependency-light: the point was to understand the primitive, not wrap someone else's.<br>
<a href="https://github.com/prajwal2308/hyper-orchestrator">source</a></td></tr>

<tr><td><strong>Thinker–<br>Curator</strong><br><sub>graduate research</sub></td>
<td>A model only sees a limited window, and as a conversation grows things fall out of it — but the model doesn't know which of them mattered. Existing answers are either reactive (retrieve once asked) or naive (store everything). Here a <strong>Thinker</strong> proposes salient facts as the conversation happens and a <strong>Curator</strong> scores what gets admitted. Their disagreement is the mechanism, not a bug.<br>
<a href="https://github.com/prajwal2308/Proactive_Retrieval_Thinker_Curator_Model_for_AI_Memory">source</a></td></tr>
</table>

<details>
<summary><strong>$ kubectl get deployments --all-namespaces</strong></summary>
<br>

- **[Cloud Microservices Platform](https://github.com/prajwal2308/cloud-microservices-platform)** — Node gateway, Go auth and Python data services on EKS, provisioned end to end in Terraform with ALB, RDS replicas, ElastiCache, Prometheus and Grafana.
- **[Real-time AI Analytics](https://github.com/prajwal2308/realtime-ai-analytics)** — Streaming ingest with ML anomaly detection, WebSocket live feed, TimescaleDB persistence.
- **[LoRaWAN Mesh Simulator](https://github.com/prajwal2308/DIS_Final_Project_LoRAWAN)** — Four containerised multi-hop UDP mesh implementations benchmarked under fault injection.

</details>

---

## Career, as a trace

```console
$ otel trace career --service prajwal --since 2023-02

SPAN                                                          START    DURATION
├─ csg-international ·············· software developer         2023-02  ███████████░░░░░░░░░░░  18mo
│    Customer Connect, the agent desktop used by global telecom carriers.
│    Cut post-release defect rates 20% via coverage and release review.
│
├─ rutgers ························ graduate teaching assistant 2024-09 ░░░░░░░░████████████░░  21mo
│    200+ students in web technologies and SQL. Code review, live debugging.
│
├─ beunec-technologies ············ cloud & systems eng, lead   2025-05 ░░░░░░░░░░░███████████  active
│    Beunec Cloud: Next.js + two distributed backends across AWS and GCP,
│    1k+ users at 99.9% availability. Global load balancing and automated
│    multi-region failover via Cloudflare. Redis in front of MongoDB to kill
│    a session-read bottleneck. Aselius AI: GenAI engine, E2E encrypted, GDPR.
│
└─ universal-selfcare ············· cloud systems eng, lead     2025-12  ░░░░░░░░░░░░░░░░░░░█░  2mo
     Serverless GCP (Cloud Functions, Cloud Run, GKE) at 95% test coverage
     in four weeks. Led five developers to a 100% on-time MVP.

status: 200 OK · errors: 0 · spans still open: 1
```

---

## SLOs I've actually hit

```console
$ kubectl top engineer prajwal

METRIC                          VALUE    CONTEXT
uptime                          99.9%    1k+ users, AWS + GCP, Cloudflare failover
orchestration-speedup            4.2×     measured against sequential execution
test-coverage                     95%     serverless GCP, inside a 4-week contract
defect-rate-delta                -20%     agent desktop, global telecom carriers
students-taught                   200+    web technologies and SQL, Rutgers
hackathon-placement               1st     AESIA × UN Tech Over
```

---

## Resource limits

```yaml
languages:   [python, typescript, javascript, go, swift, java, sql, bash]

cloud:
  platforms: [aws, gcp]
  orchestration: [kubernetes, eks, gke, helm, docker]
  iac: [terraform, github-actions, cloudflare]

ai:
  frameworks: [langchain, mcp, pytorch]
  retrieval: [rag, vector-search]
  providers: [openai, anthropic]

data:        [postgresql, mongodb, redis, kafka]
product:     [nextjs, react, node-express, fastapi, flask, swiftui, tailwind]
protocols:   [rest, grpc, sse]
systems:     [distributed-systems, system-design, microservices,
              load-balancing, failover, opentelemetry, prometheus, grafana]

education:
  - {degree: MS Computer Science, school: Rutgers–New Brunswick, gpa: 3.71/4.0, year: 2026}
  - {degree: BE Computer Science, school: MVJ College of Engineering, gpa: 9.1/10, year: 2023}
certifications: [aws-cloud-practitioner, salesforce-developer-catalyst]
```

---

```console
$ curl -s https://prajwal2308.github.io/api/availability

{
  "open_to":      ["software", "platform", "cloud/devops", "ai engineering"],
  "location":     "United States",
  "relocation":   true,
  "authorization":"F-1 OPT · STEM extension eligible",
  "contact":      "prajwal.srinivas238@gmail.com",
  "response_time":"same day"
}
```
