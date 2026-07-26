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

## 🧭 Projects at a glance

<!-- Keep this table in sync with the sections below.
     If a private repo ever goes public: link the name and change its Status to "Public".
     New row template:
     | **[name](https://github.com/The2oser-dev/name)** | One-liner | Stack | **Public** |
-->

| Project | One-liner | Stack | Status |
|:--|:--|:--|:--:|
| **[TokenEater](https://github.com/The2oser-dev/TokenEater)** | Multi-agent LLM pipeline with automatic answer verification | Python · OpenRouter | **Public** |
| **signal-hub** | Event-driven crypto trading-signals platform | Go · Python · NATS · TimescaleDB | Private |
| **fyra-portal** | Multi-model AI chat portal with credit-ledger billing | TypeScript · Next.js · Prisma | Private |
| **scanner** | Web-app vulnerability scanner with a Telegram front-end | Python | Private |
| **MyCryBot** | Bybit futures anomaly scanner — alert-only | Python · asyncio | Private |

Details on the three main systems below; the rest live in [the lab](#-in-the-lab).

## 🔬 Case studies

### [TokenEater](https://github.com/The2oser-dev/TokenEater) · Public

*Experimental multi-agent LLM pipeline with automatic answer verification.*

**Problem.** A single LLM call on a complex request fails in unpredictable ways — and free-tier models fail more often than most. Blind retries don't help when nothing checks *what* went wrong.

**Approach.** A gatekeeper decides whether the request needs decomposition, a planner splits it into subtasks, worker agents (each drawing a model from a pool of free OpenRouter models) execute them, and a verifier grades every output against explicit criteria — feeding its critique back to the worker until the subtask passes, before final assembly. Agents communicate through strict JSON contracts, with defensive parsing for the ways models actually misbehave (markdown-fenced JSON included).

**Stack.** `Python` · `OpenAI SDK → OpenRouter` · `free-tier model pool`

*Status: a working experiment and my sandbox for orchestration ideas — currently being hardened (packaging, bounded retries, explicit clarification handling).*

### signal-hub · Private
<!-- if this repo ever goes public, replace the heading above with:
### [signal-hub](https://github.com/The2oser-dev/signal-hub) · Public
and update the table row -->

*Event-driven crypto trading-signals platform.*

**Problem.** Funding-rate arbitrage and volume anomalies are only visible if you watch many markets at once, in real time — a signal delivered late is worthless.

**Approach.** Go collectors hold WebSocket connections to exchange feeds — per-connector backoff, read deadlines, per-symbol throttling — and stream market data into NATS. Strategy engines subscribe to detect funding-rate arbitrage (normalized across different funding intervals) and volume anomalies (z-score detection with cooldowns and dedup). A FastAPI backend, a Next.js web app, and a Telegram bot deliver signals with plan-based access, Stripe billing, and a referral program.

**Stack.** `Go` · `Python / FastAPI` · `TypeScript / Next.js` · `NATS` · `TimescaleDB` · `Redis` · `Docker Compose`

### fyra-portal · Private
<!-- if this repo ever goes public, replace the heading above with:
### [fyra-portal](https://github.com/The2oser-dev/fyra-portal) · Public
and update the table row -->

*Multi-model AI chat portal where the hard part is the metering.*

**Problem.** Selling LLM access is mostly a billing problem: every streamed token has to be counted, priced, and settled — without drift, and without trusting the client.

**Approach.** SSE-streamed chat proxied through an OpenAI-compatible upstream, with usage accumulated server-side while deltas stream to the browser. Per-token credit accounting on an append-only ledger, updated in the same transaction as the cached balance. Crypto subscription payments with signature-verified, idempotent webhooks and a raw-payload audit log. Session tokens stored only as hashes; rate limiting on auth routes.

**Stack.** `TypeScript` · `Next.js (App Router)` · `React` · `Prisma` · `Redis` · `Zod` · `Tailwind CSS`

## 🧪 In the lab

Smaller private projects, in brief:

<details>
<summary><b>scanner</b> — web-application security scanner with a Telegram front-end · Python</summary>

<br>

Checks security headers, TLS, technology/CVE fingerprinting, and exposed secrets, and runs common injection probes — with TXT/HTML reports delivered through a bilingual Telegram front-end. For authorized targets only.

**Stack.** `Python` · `requests` · `python-telegram-bot`

<!-- if this repo ever goes public: link the name in the summary to https://github.com/The2oser-dev/scanner -->

</details>

<details>
<summary><b>MyCryBot</b> — Bybit futures anomaly scanner, alert-only by design · Python / asyncio</summary>

<br>

Async scanner for Bybit USDT perpetuals: flags pump/dump moves using multi-timeframe RSI plus order-book and open-interest context, and sends Telegram alerts. It never places trades.

**Stack.** `Python` · `asyncio` · `pandas`

<!-- if this repo ever goes public: link the name in the summary to the repo -->

</details>

## 🛠️ How I build

- **Verify, then trust.** Model output gets graded against explicit criteria and retried with critique — not accepted on the first pass.
- **Contracts between components.** Strict JSON schemas at agent boundaries, and defensive parsing for real-world API and model quirks.
- **Events over polling.** Market data moves through a message bus so collectors, strategies, and delivery can evolve independently.
- **Build the boring parts well.** Webhook signature verification, append-only ledgers, reconnect/backoff logic — the code that makes an automated system safe to leave running.

## 📌 Now

<!-- keep this section current or delete it — a stale "Now" is worse than none -->

- Hardening **TokenEater**: packaging, bounded retries, explicit clarification handling
- Building in private — the interesting parts get written up here

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

<div align="center"><sub>Account started August 2025 — new profile, existing codebase. Most of the work is private; the write-ups above cover what the code does. GitHub is the only channel for now.</sub></div>
