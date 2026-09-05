<!--
  ─────────────────────────────────────────────────────────────
  Naman Jain — GitHub profile README
  Every number and link below is verifiable. Please keep it that way.
  ─────────────────────────────────────────────────────────────
-->

<img src="https://raw.githubusercontent.com/namanjain24-sudo/namanjain24-sudo/main/cards/hero.svg" alt="Naman Jain — I build LLM systems that ship with evaluations, not vibes." width="100%"/>

<p align="center">
  <a href="https://www.linkedin.com/in/naman-jain-067601323/"><img src="https://img.shields.io/badge/LinkedIn-Naman_Jain-0a66c2?style=flat-square&logo=linkedin&logoColor=white&labelColor=161b22" alt="LinkedIn"/></a>
  <a href="mailto:naman.2024@nst.rishihood.edu.in"><img src="https://img.shields.io/badge/Email-get_in_touch-58a6ff?style=flat-square&logo=gmail&logoColor=white&labelColor=161b22" alt="Email"/></a>
  <a href="https://www.npmjs.com/package/easycron-cli"><img src="https://img.shields.io/npm/v/easycron-cli?style=flat-square&logo=npm&logoColor=white&label=easycron-cli&labelColor=161b22&color=3fb950" alt="easycron-cli on npm"/></a>
  <a href="https://archforge.vercel.app"><img src="https://img.shields.io/badge/Live_demo-archforge-a371f7?style=flat-square&logo=vercel&logoColor=white&labelColor=161b22" alt="ArchForge live demo"/></a>
  <a href="https://www.kaggle.com/namanjain2108"><img src="https://img.shields.io/badge/Kaggle-namanjain2108-20beff?style=flat-square&logo=kaggle&logoColor=white&labelColor=161b22" alt="Kaggle"/></a>
</p>

---

Undergrad at Newton School of Technology, Rishihood University. I care about the unglamorous half of AI engineering — **making a model's output checkable**. Most of what I build ends up being a verification layer wrapped around an LLM, plus the benchmark that proves it works.

---

## What I'm building right now

### [verbatim](https://github.com/namanjain24-sudo/verbatim) — meeting intelligence for Hinglish calls

Otter, Fireflies and Fathom all fall apart on Hindi–English code-switching, and independent testing has found hallucinated content in a meaningful share of AI-generated meeting summaries. verbatim takes the opposite stance: **cite-or-drop.** Every minute, decision and action item carries a timestamped citation back to the transcript — and any claim it cannot ground gets deleted rather than guessed.

```
precision   100%    ← zero invented claims on the adversarial set
recall      91–93%
grounding   100%    ← every surviving claim carries a citation
cost        ~$0.08 / meeting-hour, self-hosted
```

Groq Whisper v3-turbo for transcription · `gpt-oss-120b` for extraction · sherpa-onnx for local speaker diarization · Qdrant + fastembed for cross-meeting RAG · RapidFuzz to validate every citation · Playwright bot that auto-joins Google Meet. Runs on your own machine, so the audio never leaves it.

`Python` `FastAPI` `Pydantic` `Qdrant` `Playwright` · MIT

---

## Selected work

### [ArchForge](https://github.com/namanjain24-sudo/archforge) — plain English → production system architecture
[**archforge.vercel.app**](https://archforge.vercel.app) · live

Type *"a ride-sharing platform"*, get a verified 15–20 component architecture with capacity math (QPS, storage, bandwidth), per-component reasoning, and a Well-Architected review across all six AWS pillars. Three deterministic verification layers sit between the model and the canvas, so it cannot emit a structurally invalid diagram. **Benchmarked at 98% recall** against the real published architectures of Uber, Instagram and Netflix. 75 tests. Exports to PNG, Mermaid or Markdown.

`React` `Vite` `React Flow` `Node` `Express` `elkjs` · Groq / Cerebras / Gemini with automatic failover

### [easycron](https://github.com/namanjain24-sudo/easycron) — cron that survives free-tier hosting
[**npm i -g easycron-cli**](https://www.npmjs.com/package/easycron-cli) · v3.0.2 published

Render, Railway and Fly.io put free instances to sleep and kill background jobs, which quietly breaks every in-process scheduler. easycron takes a schedule in plain English, compiles it to cron, and wires up an *external* trigger — GitHub Actions, UptimeRobot or cron-job.org — so the job actually fires. Plugin system with regex-safety validation, configurable retry backoff, execution logs, and endpoint scaffolding for Express and Fastify. The README documents the real limits too: the 60-day Actions sleep and the 2,000-minute monthly budget.

`Node.js` `npm` `GitHub Actions`

### [Email SDK](https://github.com/namanjain24-sudo/Email_sdk) — a delivery pipeline built to fail well
Multi-provider email delivery across AWS SES, SMTP and SendGrid, written to make the resilience patterns explicit rather than hidden: per-provider circuit breakers, token-bucket rate limiting, exponential-backoff retries, a priority queue holding 10,000 jobs drained by five concurrent workers, a dead-letter queue for what still fails, and event-based observability throughout. Documented with sequence, activity, class and use-case diagrams.

`TypeScript` `Vitest` `nodemailer` `Handlebars`

### Also built
[**Solar forecasting + agentic grid optimisation**](https://github.com/namanjain24-sudo/Solar-power-forecasting-ml) — ML forecast of solar DC output, feeding a retrieval agent that returns structured grid recommendations · [**CryptoVision**](https://crypto-vision-ecru.vercel.app/) — crypto analytics dashboard with a live market ticker · [**FairMarket India**](https://system-hackathon-website.vercel.app) — systems-thinking study of small sellers on Indian e-commerce, with causal loop and stock-flow models · [**geo-panorama-viewer**](https://geo-panorama-viewer.vercel.app) — 360° panoramas on a map, exportable as GeoJSON

---

## Open source

Contributions to projects I don't own — all verifiable:

| PR | Project | Status |
|---|---|---|
| [asyncapi/website#4403](https://github.com/asyncapi/website/pull/4403) | Made the Case Studies table responsive on mobile | **Merged** |
| [asyncapi/.github#358](https://github.com/asyncapi/.github/pull/358) | Fixed every stale link in `CONTRIBUTING.md` | **Merged** |
| [ruxailab/RUXAILAB#2346](https://github.com/ruxailab/RUXAILAB/pull/2346) | Scoped the "Remember me" opt-out to the browser session | Open |
| [ruxailab/RUXAILAB#2348](https://github.com/ruxailab/RUXAILAB/pull/2348) | Send signed-out visitors to sign-in before a study | Open |

---

## Stack

**Languages** &nbsp;Python · TypeScript · JavaScript · HTML/CSS

**AI systems** &nbsp;Groq · Whisper · RAG with Qdrant + fastembed · speaker diarization (sherpa-onnx) · eval harnesses & grounding checks

**Backend** &nbsp;FastAPI · Pydantic · Node.js · Express · queues, retries, circuit breakers, rate limiting

**Frontend** &nbsp;React · Vite · Tailwind · React Flow

**Tooling** &nbsp;Git · GitHub Actions · Vercel · Playwright · Vitest

---

<div align="center">

**Open to internships and to collaborating on open source.**<br/>
Best way to reach me: [naman.2024@nst.rishihood.edu.in](mailto:naman.2024@nst.rishihood.edu.in)

</div>
