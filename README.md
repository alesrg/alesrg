<div align="center">

# The2oser

### Engineering behind the scenes: event-driven backends, payments that reconcile, and systems built to keep running — with LLM agents as one tool among many.

<br>

<img src="https://img.shields.io/badge/Python-1a1b27?style=for-the-badge&logo=python&logoColor=7aa2f7" alt="Python" />
<img src="https://img.shields.io/badge/TypeScript-1a1b27?style=for-the-badge&logo=typescript&logoColor=7aa2f7" alt="TypeScript" />
<img src="https://img.shields.io/badge/Go-1a1b27?style=for-the-badge&logo=go&logoColor=7aa2f7" alt="Go" />
<img src="https://img.shields.io/badge/NATS-1a1b27?style=for-the-badge&logo=natsdotio&logoColor=7aa2f7" alt="NATS" />
<img src="https://img.shields.io/badge/Redis-1a1b27?style=for-the-badge&logo=redis&logoColor=7aa2f7" alt="Redis" />
<img src="https://img.shields.io/badge/Docker-1a1b27?style=for-the-badge&logo=docker&logoColor=7aa2f7" alt="Docker" />

</div>

---

- **What I build:** backend systems that process data and money end-to-end — market-data ingestion, signal detection, and the billing layer that turns an automated system into a product.
- **How:** event-driven architecture on a message bus, typed contracts between services, and the unglamorous guarantees that make automation safe to leave running — reconnect/backoff, idempotent webhooks, append-only ledgers, rate limiting, payment reconciliation.
- **AI where it earns it:** LLM agents as a component inside pipelines (planner / worker / verifier) — not the whole story, just another service in the system.

## 🚀 Featured projects

<!-- Template for adding a new project section:
### [name](https://github.com/The2oser-dev/name)
*One-liner.*
**Problem.** ...
**Approach.** ...
**Stack.** `...` · `...`
-->

### [TokenEater](https://github.com/The2oser-dev/TokenEater)

*An experimental multi-stage pipeline where LLM agents cooperate as a team — a hands-on sandbox for orchestration and reliable automation.*

**Problem.** A single LLM call on a complex request fails in unpredictable ways, and free-tier models fail more often than most. Blind retries don't help when nothing checks *what* went wrong — the same reliability problem you meet in any distributed system.

**Approach.** A gatekeeper decides whether the request needs decomposition, a planner splits it into subtasks, worker agents (each drawing a model from a pool of free OpenRouter models) execute them, and a verifier grades every output against explicit criteria — feeding critique back to the worker until it passes, before final assembly. Agents communicate through strict JSON contracts, with defensive parsing for the ways models actually misbehave (markdown-fenced JSON included). Structurally, it's the same contract-and-verify pattern I'd use between any two services.

**Stack.** `Python` · `OpenAI SDK → OpenRouter` · `free-tier model pool`

*Status: a working experiment and my sandbox for orchestration ideas. More projects in other stacks are being published.*

## 🛠️ How I build

- **Contract-first.** Every service boundary speaks strict, typed contracts — parsed defensively against the real world, whether that's a flaky API or a misbehaving model.
- **Events over polling.** Data flows through a message bus so collectors, strategies, and delivery can evolve independently.
- **Reliability by default.** Reconnect/backoff, idempotent webhooks, append-only ledgers, and reconciliation — the code that lets an automated system run unattended.
- **Verify, then trust.** Output gets graded and retried with critique — never accepted on the first pass.

## 📌 Now

- Hardening **TokenEater** (packaging, bounded retries, explicit clarification handling)
- Building the next public projects in other stacks to round out the portfolio

<sub>Updated August 2026</sub>

## 🧰 Toolbox

<div align="center">

<img src="https://skillicons.dev/icons?i=py,ts,go,react,nextjs,fastapi,prisma,redis,postgres,docker,tailwind&theme=dark" alt="Python, TypeScript, Go, React, Next.js, FastAPI, Prisma, Redis, PostgreSQL, Docker, Tailwind CSS" />

</div>

**Languages** — Python · TypeScript · Go<br>
**Backend & systems** — FastAPI · event-driven architecture · message buses (NATS) · Redis · PostgreSQL / TimescaleDB · Docker<br>
**Web & product** — React · Next.js · Tailwind · Prisma<br>
**AI & agents** — OpenAI-compatible APIs · OpenRouter · multi-agent orchestration · verification loops<br>
**Infra & payments** — Docker Compose · Stripe · NOWPayments · reconciliation

---

<div align="center"><sub>Account started August 2025. GitHub is the only channel for now.</sub></div>
