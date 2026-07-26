<div align="center">

# The2oser

### I build LLM agent pipelines that check their own work — and trading infrastructure to point them at.

<br>

<img src="https://img.shields.io/badge/Python-1a1b27?style=for-the-badge&logo=python&logoColor=7aa2f7" alt="Python" />
<img src="https://img.shields.io/badge/TypeScript-1a1b27?style=for-the-badge&logo=typescript&logoColor=7aa2f7" alt="TypeScript" />
<img src="https://img.shields.io/badge/Go-1a1b27?style=for-the-badge&logo=go&logoColor=7aa2f7" alt="Go" />
<img src="https://img.shields.io/badge/NATS-1a1b27?style=for-the-badge&logo=natsdotio&logoColor=7aa2f7" alt="NATS" />
<img src="https://img.shields.io/badge/Redis-1a1b27?style=for-the-badge&logo=redis&logoColor=7aa2f7" alt="Redis" />
<img src="https://img.shields.io/badge/Docker-1a1b27?style=for-the-badge&logo=docker&logoColor=7aa2f7" alt="Docker" />

</div>

---

- Core focus: **multi-agent LLM orchestration** — planner / worker / verifier loops, strict JSON contracts between agents, critique-and-retry when an output fails verification
- Applied domain: **crypto market automation** — exchange market-data ingestion, signal detection, and the billing that turns an AI system into a product
- Bias toward the unglamorous parts: reconnect/backoff logic, idempotent webhooks, append-only ledgers, rate limiting

## 🔬 Featured project

<!-- Template for adding a new project section:
### [name](https://github.com/The2oser-dev/name)
*One-liner.*
**Problem.** ...
**Approach.** ...
**Stack.** `...` · `...`
-->

### [TokenEater](https://github.com/The2oser-dev/TokenEater)

*Experimental multi-agent LLM pipeline with automatic answer verification.*

**Problem.** A single LLM call on a complex request fails in unpredictable ways — and free-tier models fail more often than most. Blind retries don't help when nothing checks *what* went wrong.

**Approach.** A gatekeeper decides whether the request needs decomposition, a planner splits it into subtasks, worker agents (each drawing a model from a pool of free OpenRouter models) execute them, and a verifier grades every output against explicit criteria — feeding its critique back to the worker until the subtask passes, before final assembly. Agents communicate through strict JSON contracts, with defensive parsing for the ways models actually misbehave (markdown-fenced JSON included).

**Stack.** `Python` · `OpenAI SDK → OpenRouter` · `free-tier model pool`

*Status: a working experiment and my sandbox for orchestration ideas — currently being hardened (packaging, bounded retries, explicit clarification handling).*

## 🛠️ How I build

- **Verify, then trust.** Model output gets graded against explicit criteria and retried with critique — not accepted on the first pass.
- **Contracts between components.** Strict JSON schemas at agent boundaries, and defensive parsing for real-world API and model quirks.
- **Events over polling.** Market data moves through a message bus so collectors, strategies, and delivery can evolve independently.
- **Build the boring parts well.** Webhook signature verification, append-only ledgers, reconnect/backoff logic — the code that makes an automated system safe to leave running.

## 📌 Now

<!-- keep this section current or delete it — a stale "Now" is worse than none -->

- Hardening **TokenEater**: packaging, bounded retries, explicit clarification handling

<sub>Updated July 2026</sub>

## 🧰 Toolbox

<div align="center">

<img src="https://skillicons.dev/icons?i=py,ts,go,react,nextjs,fastapi,prisma,redis,postgres,docker,tailwind&theme=dark" alt="Python, TypeScript, Go, React, Next.js, FastAPI, Prisma, Redis, PostgreSQL, Docker, Tailwind CSS" />

</div>

**Languages** — Python · TypeScript · Go<br>
**LLM & agents** — OpenAI-compatible APIs · OpenRouter · multi-agent orchestration · structured-output prompting · verification loops<br>
**Backend & data** — FastAPI · Next.js · Prisma · NATS · Redis · PostgreSQL / TimescaleDB · pandas<br>
**Infra & payments** — Docker Compose · Stripe · NOWPayments

---

<div align="center"><sub>Account started August 2025. GitHub is the only channel for now.</sub></div>
