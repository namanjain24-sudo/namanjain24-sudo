<!--
  ─────────────────────────────────────────────────────────────
  Naman Jain — GitHub profile README
  Every number and link below is verifiable. Please keep it that way.
  ─────────────────────────────────────────────────────────────
-->

<img src="https://raw.githubusercontent.com/namanjain24-sudo/namanjain24-sudo/main/cards/hero.svg" alt="Naman Jain — I build LLM systems that ship with evaluations, not vibes." width="100%"/>

<p align="center">
  <a href="https://naman-potfolio.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-naman--potfolio-1f6feb?style=flat-square&logo=vercel&logoColor=white&labelColor=161b22" alt="Portfolio"/></a>
  <a href="https://drive.google.com/file/d/1jZePl_IdUgjF6UG0PMg7UYAuYk1ruQp9/view?usp=sharing"><img src="https://img.shields.io/badge/R%C3%A9sum%C3%A9-PDF-d29922?style=flat-square&logo=googledrive&logoColor=white&labelColor=161b22" alt="Resume"/></a>
  <a href="https://www.linkedin.com/in/naman-jain-067601323/"><img src="https://img.shields.io/badge/LinkedIn-Naman_Jain-0a66c2?style=flat-square&logo=linkedin&logoColor=white&labelColor=161b22" alt="LinkedIn"/></a>
  <a href="mailto:namanjainpy@gmail.com"><img src="https://img.shields.io/badge/Email-namanjainpy%40gmail.com-58a6ff?style=flat-square&logo=gmail&logoColor=white&labelColor=161b22" alt="Email"/></a>
  <a href="https://www.npmjs.com/package/easycron-cli"><img src="https://img.shields.io/npm/v/easycron-cli?style=flat-square&logo=npm&logoColor=white&label=easycron-cli&labelColor=161b22&color=3fb950" alt="easycron-cli on npm"/></a>
  <a href="https://www.kaggle.com/namanjain2108"><img src="https://img.shields.io/badge/Kaggle-namanjain2108-20beff?style=flat-square&logo=kaggle&logoColor=white&labelColor=161b22" alt="Kaggle"/></a>
</p>

---

Full-stack engineer working on GenAI applications. B.Tech in Computer Science and Artificial Intelligence at **Newton School of Technology, Rishihood University** (2024–2028).

I care about the unglamorous half of AI engineering — **making a model's output checkable**. Most of what I build ends up being a verification layer wrapped around an LLM, plus the benchmark that proves it works.

---

## Experience

**GenAI Trainer** — Octa Learning · *Aug 2025 – present*
Teaching applied generative AI to 20+ students: LLMs, retrieval-augmented generation and prompt engineering. Designed the hands-on projects where learners build and integrate real AI-powered applications.

**Full-Stack Developer**, freelance · *Jan 2025 – present*
Delivered production web applications for 10+ clients, most of them live with real users. Backend systems and REST APIs, deployed end to end — owned from requirements through to keeping them running.

**Software Engineer Intern** — Klariti Learning Innovations · *May 2025 – Jul 2025*
Built full-stack features on a React and Node.js ed-tech platform used by students and instructors. Shipped REST APIs for user accounts and course workflows serving thousands of requests a day, and cut frontend load time through component-level optimisation.

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

### [Nova](https://github.com/namanjain24-sudo/nova) — a visual website builder for the browser
Drag blocks onto a canvas, style them in an inspector, and export a real, dependency-free site as HTML or React. Built as a full editor rather than a demo: 46 blocks, 24 starter templates, responsive breakpoints, reusable components, undo/redo, a command palette, accounts, one-click publishing, and form submissions collected in a real backend.

`React` `TypeScript` `Vite` · MIT

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
[**Solar forecasting + agentic grid optimisation**](https://github.com/namanjain24-sudo/Solar-power-forecasting-ml) — ML forecast of solar DC output, feeding a retrieval agent that returns structured grid recommendations · [**CryptoVision**](https://crypto-vision-ecru.vercel.app/) — crypto analytics dashboard with a live market ticker · [**FairMarket India**](https://system-hackathon-website.vercel.app) — systems-thinking study of small sellers on Indian e-commerce, with causal loop and stock-flow models · [**geo-panorama-viewer**](https://geo-panorama-viewer.vercel.app) — 360° panoramas on a map, exportable as GeoJSON · [**HomeScope360**](https://home-scope360-hpgl.vercel.app/) — real-estate platform with 360° virtual property tours

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

**Languages** &nbsp;JavaScript · TypeScript · Python

**AI / ML** &nbsp;LLMs · RAG · prompt engineering · vector databases · PyTorch · eval harnesses and grounding checks

**Frontend** &nbsp;React · Next.js · Vite · Tailwind · React Flow

**Backend** &nbsp;Node.js · Express · FastAPI · Pydantic · REST APIs · microservices · queues, retries, circuit breakers, rate limiting

**Data** &nbsp;PostgreSQL · MongoDB · Qdrant · NumPy · Pandas

**Concepts** &nbsp;Distributed systems · API design · caching · async processing

**Tooling** &nbsp;Git · GitHub Actions · Docker · Vercel · Postman · Playwright · Vitest

---

<div align="center">

**Open to internships and to collaborating on open source.**<br/>
[namanjainpy@gmail.com](mailto:namanjainpy@gmail.com) &nbsp;·&nbsp; [Portfolio](https://naman-potfolio.vercel.app/) &nbsp;·&nbsp; [Résumé](https://drive.google.com/file/d/1jZePl_IdUgjF6UG0PMg7UYAuYk1ruQp9/view?usp=sharing) &nbsp;·&nbsp; [LinkedIn](https://www.linkedin.com/in/naman-jain-067601323/)

</div>
