<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1b27,100:7aa2f7&height=150&section=header&text=AlesRG&fontSize=54&fontColor=e2e2e2&desc=local-first%20AI%20infrastructure&descSize=17&descAlignY=66" width="100%" alt="header"/>

<a href="https://github.com/alesrg">
<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=21&duration=2800&pause=900&color=7AA2F7&center=true&vCenter=true&width=720&lines=I+make+free+LLMs+actually+usable;OpenAI-compatible+proxies+%C2%B7+multi-agent+pipelines;Token+observability+%C2%B7+local-first+by+design" alt="typing"/>
</a>

<img src="https://skillicons.dev/icons?i=py,nodejs,js,flask,sqlite,docker,git&theme=dark" alt="stack"/>

</div>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" alt="divider"/>

## Projects

| Project | What it does | Stack |
|---|---|---|
| [**TokenEater**](https://github.com/alesrg/TokenEater) <sub>![stars](https://img.shields.io/github/stars/alesrg/TokenEater?style=flat&label=%E2%98%85&labelColor=1a1b27&color=7aa2f7)</sub> | Multi-agent pipeline where LLMs work as a team: gatekeeper → planner → workers → verifier. Weak free models get stronger through strict JSON contracts and automatic answer correction — retries that know *why* they retry. | `Python` `OpenRouter` |
| [**FreeQwenApi**](https://github.com/alesrg/FreeQwenApi) <sub>![stars](https://img.shields.io/github/stars/alesrg/FreeQwenApi?style=flat&label=%E2%98%85&labelColor=1a1b27&color=7aa2f7)</sub> | Local OpenAI-compatible proxy for Qwen Chat: any model ID passes through as-is, multi-account rotation, files, image & video generation. Plugs into Open WebUI, LiteLLM, coding agents. | `Node.js` `Express` |
| [**cline-api**](https://github.com/alesrg/cline-api) <sub>![stars](https://img.shields.io/github/stars/alesrg/cline-api?style=flat&label=%E2%98%85&labelColor=1a1b27&color=7aa2f7)</sub> | HTTP bridge that exposes the Cline coding agent as an OpenAI-compatible API: SSE streaming, file attachments, optional agent tools — zero runtime dependencies. | `Node.js` `SSE` |
| [**llm-token-dashboard**](https://github.com/alesrg/llm-token-dashboard) <sub>![stars](https://img.shields.io/github/stars/alesrg/llm-token-dashboard?style=flat&label=%E2%98%85&labelColor=1a1b27&color=7aa2f7)</sub> | Web dashboard for token usage collected from local AI tools (Hermes, OpenCode). Reads only your own SQLite — if tokens flow, they get counted. | `Python` `Flask` `SQLite` |

## How I think about it

- **Contract-first.** Every boundary — between services or between agents — speaks strict typed contracts, parsed defensively against the way models *actually* misbehave.
- **Local-first.** Your account, your keys, your data on your disk. A proxy should be boring infrastructure, not a SaaS.
- **Verification over vibes.** Free-tier models fail more often; blind retries don't fix that. Check *what* broke, critique, retry — then assemble.

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" alt="divider"/>

<div align="center">

## GitHub Stats

<img height="165" src="https://github-readme-stats.vercel.app/api?username=alesrg&show_icons=true&hide_border=true&bg_color=00000000&title_color=7aa2f7&icon_color=7aa2f7&text_color=c0caf5" alt="stats"/>
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=alesrg&layout=compact&hide_border=true&bg_color=00000000&title_color=7aa2f7&text_color=c0caf5" alt="top langs"/>

<br>

[![streak](https://streak-stats.demolab.com?user=alesrg&locale=en&mode=weekly&hide_border=true&background=00000000&ring=7aa2f7&fire=E8B34B&currStreakLabel=7aa2f7)](https://github.com/alesrg)

<br>

<img src="https://raw.githubusercontent.com/alesrg/alesrg/output/github-snake-dark.svg" alt="contribution snake" width="100%"/>

<br>

*Building in public — issues and PRs are always open.*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:7aa2f7,100:1a1b27&height=110&section=footer" width="100%" alt="footer"/>

</div>
