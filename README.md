<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1b27,100:7aa2f7&height=150&section=header&text=AlesRG&fontSize=54&fontColor=e2e2e2&desc=local-first%20AI%20infrastructure&descSize=17&descAlignY=66" width="100%" alt="header"/>

**[English](#i-make-free-llms-actually-usable)** · **[Русский](#делаю-бесплатные-llm-по-настоящему-рабочими)**

### I make free LLMs actually usable

**OpenAI-compatible proxies · multi-agent pipelines · token observability — everything runs locally, no cloud middleman.**

<br>

<img src="https://img.shields.io/badge/Python-1a1b27?style=for-the-badge&logo=python&logoColor=7aa2f7" alt="Python"/>
<img src="https://img.shields.io/badge/JavaScript-1a1b27?style=for-the-badge&logo=javascript&logoColor=7aa2f7" alt="JavaScript"/>
<img src="https://img.shields.io/badge/Node.js-1a1b27?style=for-the-badge&logo=nodedotjs&logoColor=7aa2f7" alt="Node.js"/>
<img src="https://img.shields.io/badge/Flask-1a1b27?style=for-the-badge&logo=flask&logoColor=7aa2f7" alt="Flask"/>
<img src="https://img.shields.io/badge/OpenAI_API-1a1b27?style=for-the-badge&logo=openai&logoColor=7aa2f7" alt="OpenAI API"/>
<img src="https://img.shields.io/badge/Docker-1a1b27?style=for-the-badge&logo=docker&logoColor=7aa2f7" alt="Docker"/>

</div>

---

## 🧩 Projects

<table>
<tr>
<td width="50%" valign="top">

### 🤖 [TokenEater](https://github.com/alesrg/TokenEater)

Multi-agent pipeline where LLMs work as a team: gatekeeper → planner → workers → verifier. Weak free models get stronger through strict JSON contracts and automatic answer correction — retries that know *why* they retry.

![stars](https://img.shields.io/github/stars/alesrg/TokenEater?style=flat&label=%E2%98%85&labelColor=1a1b27&color=7aa2f7)
![lang](https://img.shields.io/badge/Python-1a1b27?style=flat-square&logo=python&logoColor=7aa2f7)
![topic](https://img.shields.io/badge/OpenRouter-1a1b27?style=flat-square&labelColor=1a1b27&color=24283b)

</td>
<td width="50%" valign="top">

### 🔌 [FreeQwenApi](https://github.com/alesrg/FreeQwenApi)

Local OpenAI-compatible proxy for Qwen Chat: any model ID passes through as-is, multi-account rotation, files, image & video generation. Plugs into Open WebUI, LiteLLM, coding agents.

![stars](https://img.shields.io/github/stars/alesrg/FreeQwenApi?style=flat&label=%E2%98%85&labelColor=1a1b27&color=7aa2f7)
![lang](https://img.shields.io/badge/Node.js-1a1b27?style=flat-square&logo=nodedotjs&logoColor=7aa2f7)
![topic](https://img.shields.io/badge/OpenAI--compatible-1a1b27?style=flat-square&labelColor=1a1b27&color=24283b)

</td>
</tr>
<tr>
<td width="50%" valign="top">

### ⚡ [cline-api](https://github.com/alesrg/cline-api)

HTTP bridge that exposes the Cline coding agent as an OpenAI-compatible API: SSE streaming, file attachments, optional agent tools — zero runtime dependencies.

![stars](https://img.shields.io/github/stars/alesrg/cline-api?style=flat&label=%E2%98%85&labelColor=1a1b27&color=7aa2f7)
![lang](https://img.shields.io/badge/Node.js-1a1b27?style=flat-square&logo=nodedotjs&logoColor=7aa2f7)
![topic](https://img.shields.io/badge/SSE-1a1b27?style=flat-square&labelColor=1a1b27&color=24283b)

</td>
<td width="50%" valign="top">

### 📊 [llm-token-dashboard](https://github.com/alesrg/llm-token-dashboard)

Web dashboard for token usage collected from local AI tools (Hermes, OpenCode). Reads only your own SQLite — if tokens flow, they get counted.

![stars](https://img.shields.io/github/stars/alesrg/llm-token-dashboard?style=flat&label=%E2%98%85&labelColor=1a1b27&color=7aa2f7)
![lang](https://img.shields.io/badge/Python-1a1b27?style=flat-square&logo=python&logoColor=7aa2f7)
![topic](https://img.shields.io/badge/SQLite-1a1b27?style=flat-square&labelColor=1a1b27&color=24283b)

</td>
</tr>
</table>

## 🧭 How I think about it

- **Contract-first.** Every boundary — between services or between agents — speaks strict typed contracts, parsed defensively against the way models *actually* misbehave.
- **Local-first.** Your account, your keys, your data on your disk. A proxy should be boring infrastructure, not a SaaS.
- **Verification over vibes.** Free-tier models fail more often; blind retries don't fix that. Check *what* broke, critique, retry — then assemble.

---

<div align="center">

**[English](#i-make-free-llms-actually-usable)** · **Русский**

### Делаю бесплатные LLM по-настоящему рабочими

**OpenAI-совместимые прокси · мультиагентные пайплайны · учёт токенов — всё работает локально, без облачных посредников.**

</div>

## 🧩 Проекты

<table>
<tr>
<td width="50%" valign="top">

### 🤖 [TokenEater](https://github.com/alesrg/TokenEater)

Мультиагентный пайплайн, где LLM работают командой: гейткипер → планировщик → исполнители → верификатор. Слабые бесплатные модели становятся сильнее за счёт строгих JSON-контрактов и автокоррекции ответов — ретраи, которые понимают, *почему* ретраят.

![stars](https://img.shields.io/github/stars/alesrg/TokenEater?style=flat&label=%E2%98%85&labelColor=1a1b27&color=7aa2f7)
![lang](https://img.shields.io/badge/Python-1a1b27?style=flat-square&logo=python&logoColor=7aa2f7)
![topic](https://img.shields.io/badge/OpenRouter-1a1b27?style=flat-square&labelColor=1a1b27&color=24283b)

</td>
<td width="50%" valign="top">

### 🔌 [FreeQwenApi](https://github.com/alesrg/FreeQwenApi)

Локальный OpenAI-совместимый прокси для Qwen Chat: любой model ID проходит как есть, ротация нескольких аккаунтов, файлы, генерация картинок и видео. Подключается к Open WebUI, LiteLLM и кодинг-агентам.

![stars](https://img.shields.io/github/stars/alesrg/FreeQwenApi?style=flat&label=%E2%98%85&labelColor=1a1b27&color=7aa2f7)
![lang](https://img.shields.io/badge/Node.js-1a1b27?style=flat-square&logo=nodedotjs&logoColor=7aa2f7)
![topic](https://img.shields.io/badge/OpenAI--compatible-1a1b27?style=flat-square&labelColor=1a1b27&color=24283b)

</td>
</tr>
<tr>
<td width="50%" valign="top">

### ⚡ [cline-api](https://github.com/alesrg/cline-api)

HTTP-мост, который превращает Cline-агента в OpenAI-совместимый API: SSE-стриминг, вложения файлов, опциональные agent-инструменты — ноль рантайм-зависимостей.

![stars](https://img.shields.io/github/stars/alesrg/cline-api?style=flat&label=%E2%98%85&labelColor=1a1b27&color=7aa2f7)
![lang](https://img.shields.io/badge/Node.js-1a1b27?style=flat-square&logo=nodedotjs&logoColor=7aa2f7)
![topic](https://img.shields.io/badge/SSE-1a1b27?style=flat-square&labelColor=1a1b27&color=24283b)

</td>
<td width="50%" valign="top">

### 📊 [llm-token-dashboard](https://github.com/alesrg/llm-token-dashboard)

Веб-дашборд расхода токенов из локальных баз AI-инструментов (Hermes, OpenCode). Читает только ваш SQLite — если токены текут, они посчитаны.

![stars](https://img.shields.io/github/stars/alesrg/llm-token-dashboard?style=flat&label=%E2%98%85&labelColor=1a1b27&color=7aa2f7)
![lang](https://img.shields.io/badge/Python-1a1b27?style=flat-square&logo=python&logoColor=7aa2f7)
![topic](https://img.shields.io/badge/SQLite-1a1b27?style=flat-square&labelColor=1a1b27&color=24283b)

</td>
</tr>
</table>

## 🧭 Как я это делаю

- **Контракты прежде всего.** Каждая граница — между сервисами или между агентами — говорит на строгих типизированных контрактах, парсимых с защитой от реального поведения моделей.
- **Локальность прежде всего.** Ваш аккаунт, ваши ключи, ваши данные на вашем диске. Прокси — это скучная инфраструктура, а не SaaS.
- **Проверка вместо вайбов.** Бесплатные модели падают чаще; слепые ретраи не лечат. Проверить, *что именно* сломалось, покритиковать, повторить — и только потом собирать ответ.

---

<div align="center">

## 📈 GitHub Stats

<img height="165" src="https://github-readme-stats.vercel.app/api?username=alesrg&show_icons=true&hide_border=true&bg_color=00000000&title_color=7aa2f7&icon_color=7aa2f7&text_color=c0caf5" alt="stats"/>
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=alesrg&layout=compact&hide_border=true&bg_color=00000000&title_color=7aa2f7&text_color=c0caf5" alt="top langs"/>

<br>

[![streak](https://streak-stats.demolab.com?user=alesrg&locale=en&mode=weekly&hide_border=true&background=00000000&ring=7aa2f7&fire=E8B34B&currStreakLabel=7aa2f7)](https://github.com/alesrg)

*Building in public — issues and PRs are always open.*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:7aa2f7,100:1a1b27&height=110&section=footer" width="100%" alt="footer"/>

</div>
