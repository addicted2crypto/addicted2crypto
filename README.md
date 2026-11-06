<picture>
  <source media="(prefers-color-scheme: light)" srcset="./assets/profile-light.svg">
  <img src="./assets/profile-dark.svg" alt="Will / addicted2crypto — secure systems, AI engineering, and on-chain research. Building DCGP and onchaintruth." width="100%">
</picture>

<div align="center">

<h1>Hey, I’m Will.</h1>

<p><strong>AI &amp; full-stack engineer · C#/.NET · SQL &amp; data research · Security first</strong></p>

<p><code>C#</code> · <code>.NET</code> · <code>SQL</code> · <code>TypeScript</code> · <code>Python</code> · <code>JavaScript</code></p>

<p>
  <a href="https://github.com/addicted2crypto/DCGP"><strong>DCGP</strong></a> ·
  <a href="https://hcash.onchaintruth.xyz"><strong>hCASH Oracle</strong></a> ·
  <a href="https://moat.onchaintruth.xyz/leaderboard"><strong>Moat research</strong></a> ·
  <a href="https://williamsforeverportfolio.vercel.app">Portfolio</a> ·
  <a href="https://linkedin.com/in/william360">LinkedIn</a>
</p>

</div>

---

I build secure software, local AI systems, and tools that turn data into something useful. **8+ years shipping production systems**, with C#/.NET and SQL at the foundation and AI orchestration, research pipelines, and full-stack products on top.

My day job is DoD contract engineering. Outside work, I’m building **DCGP** and shipping research through **onchaintruth**. I like working through the whole problem: the context an agent sees, the tools it can call, the data behind an answer, and the application someone actually uses.

**Built it. Hardened it. Shipped it. Still learning.**

## DCGP · the governance layer

**Dynamic Context Guidance Paths — the semantic operating system for LLM agents.** My work on keeping long-running AI sessions grounded in the project they’re working on. The problem that interests me: as a session grows, how do you detect degrading context, intervene, and protect the information that still matters?

DCGP runs a **seven-step control loop** around an agent. It senses the workspace, classifies the domain, tracks context health, injects project anchors, checks output, and feeds those signals back into retention policy.

<picture>
  <source media="(max-width: 600px) and (prefers-color-scheme: light)" srcset="./assets/dcgp-loop-mobile-light.svg">
  <source media="(max-width: 600px)" srcset="./assets/dcgp-loop-mobile-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="./assets/dcgp-loop-light.svg">
  <img src="./assets/dcgp-loop-dark.svg" alt="DCGP loop: Sense, Classify, Predict, Orchestrate, Execute, Verify, Refine, then repeat. Context health informs retention through a RetentionDirective." width="100%">
</picture>

- **Context health:** five factors combine into a Health Index, with hysteresis and cooldowns controlling interventions.
- **Retention with rules:** `RetentionDirective` connects that health signal to pruning consumers; protected paths stay protected.
- **Checks you can inspect:** output gates, domain drift detection, deterministic scoring, and Sentinel tests.
- **Tools around the core:** CLI, MCP server, OpenCode integration, VS Code extension, `vibe-audit` static analysis, and a fine-tuning exporter.

The research is in the feedback loop, failure modes, and retention contract. The implementation is there to inspect, run, and challenge.

<details>
<summary>Under the hood: context health & retention</summary>

The Health Index combines gate pressure, domain drift, confidence decay, citation pressure, and session age. Its response is graduated:

| Health level | Retention directive | Retention floor |
| :--- | :--- | :--- |
| NOMINAL | PASSIVE | 0.20 |
| ELEVATED | TIGHTEN | 0.40 |
| HIGH | AGGRESSIVE | 0.65 |
| CRITICAL | NUCLEAR | 0.90 |

Consumers keep blocks that meet the floor **or** match a protected path. Hysteresis, cooldowns, and partial resets handle stability across turns and domain changes.

</details>

[Source](https://github.com/addicted2crypto/DCGP) · [Specification](https://github.com/addicted2crypto/DCGP/blob/main/DCGP-SPEC.md) · [Sentinel tests](https://github.com/addicted2crypto/DCGP/tree/main/packages/core/tests) · [Verification](https://github.com/addicted2crypto/DCGP/blob/main/scripts/verify-dcgp.sh)

## onchaintruth · research you can use

On-chain research is where I put data engineering, financial modeling, and application development together. I build the collection pipeline, work through the model, and ship an interface that makes the result useful.

I start with concrete questions: **Where is break-even? What did this strategy actually return? What was the opportunity cost?**

<picture>
  <source media="(max-width: 600px) and (prefers-color-scheme: light)" srcset="./assets/research-mobile-light.svg">
  <source media="(max-width: 600px)" srcset="./assets/research-mobile-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="./assets/research-light.svg">
  <img src="./assets/research-dark.svg" alt="Onchaintruth research workflow: collect chain and market data, model costs and benchmarks, then publish calculators and strategy comparisons. Wallet and contract research is a separate ongoing track." width="100%">
</picture>

<table>
<tr>
<td width="50%" valign="top">
<h3><a href="https://hcash.onchaintruth.xyz">hCASH ROI Oracle ↗</a></h3>
<p><strong>Where is the mining break-even?</strong></p>
<p>ROI and scenario analysis on Avalanche, bringing together AVAX/USD oracle pricing, hCASH market data, and on-chain marketplace and contract reads.</p>
<p><code>Chainlink</code> · <code>DexScreener</code> · <code>Avalanche</code></p>
</td>
<td width="50%" valign="top">
<h3><a href="https://moat.onchaintruth.xyz/leaderboard">Moat OCA / MOCA ↗</a></h3>
<p><strong>Did the strategy beat holding AVAX or BTC?</strong></p>
<p>Wallet analysis, strategy comparisons, and opportunity-cost modeling, with a leaderboard for exploring results.</p>
<p><code>Next.js</code> · <code>TypeScript</code> · <code>On-chain data</code></p>
</td>
</tr>
</table>

I want the numbers, assumptions, and benchmarks behind a result to be inspectable.

## The systems around the research

| Project | What I’m building |
| :--- | :--- |
| [WillAgent](https://github.com/addicted2crypto/willagent) | Self-hosted orchestration: local and API model routing, typed tools, audit logs, token discovery, and wallet analysis. |
| **EVMSleuth** · private | Wallet tracking, contract analysis, and token intelligence. Related research interests include threat modeling and Foundry proofs of concept. |
| [GymTech](https://github.com/addicted2crypto/gymtech) · in development | Multi-tenant gym SaaS: roles, subscriptions, billing, QR check-in, and database-enforced tier limits. |

## The background behind the builds

**Federal health & enterprise engineering.** Work across DHA.mil, health.mil, and TRICARE, with C#/.NET, Sitecore, ASP.NET MVC, and Docker. My background also includes NestJS SDK tooling and Hyperledger Iroha integrations. Security, accessibility, and operating constraints are part of the engineering work.

**From hands-on diagnostics to software.** Before software, I spent a decade in appliance repair. That habit of tracing a fault through a system still shapes how I build. Appliance Consult grew out of turning repair knowledge into a usable application.

**Security background:** CompTIA Security+ · DoD IAT II experience · secure enterprise systems.

<details>
<summary><strong>More work along the way</strong> — earlier products, experiments, and interests</summary>

| Work | Focus |
| :--- | :--- |
| **Learning Tutor** | Adaptive learning plans and LLM-assisted tutoring, originally built to support my Security+ study. |
| **Appliance Consult** | AI-assisted repair guidance, billing, and a production database. |
| **Command Center** | Development team leadership on a wallet tracker with multi-chain indexing and DeFi views. |
| **CFT** | Decentralized market pools, transaction indexing, and visibility into on-chain activity. |

More project context is on my [portfolio](https://williamsforeverportfolio.vercel.app/#projects).

</details>

## My working stack

| Area | Tools & technologies |
| :--- | :--- |
| Enterprise & backend | **C#, .NET, ASP.NET MVC, Sitecore** · Node.js, NestJS |
| Data & infrastructure | **SQL, PostgreSQL** · Redis, BullMQ, Docker, Supabase, Azure |
| AI & automation | **Python, local LLMs, Ollama** · Claude API, RAG, agents, MCP |
| Applications | **TypeScript, JavaScript, React, Next.js** · Tailwind CSS, Framer Motion |
| On-chain & security research | **Solidity, Foundry, Avalanche** · viem, wagmi, Chainlink |

<details>
<summary>Broader toolkit</summary>

Other work and experiments include Rust, Go, Java, Express, Django, MongoDB, Prisma, and Drizzle.

</details>

## What keeps me interested

- Local models doing useful work, with clear tool boundaries and a trail you can inspect.
- Context retention, RAG, and how agent behavior changes over long sessions.
- SQL-first research, oracle data, on-chain signals, and honest benchmark comparisons.
- Smart contract analysis, wallet intelligence, and adversarial testing.
- Secure SaaS, tenant isolation, and the infrastructure behind reliable applications.

## Let’s build

I’m open to work and collaboration across **AI systems, developer tooling, secure full-stack engineering, data platforms, and on-chain research**.

[Portfolio](https://williamsforeverportfolio.vercel.app) · [LinkedIn](https://linkedin.com/in/william360) · [X / @willisdeving](https://twitter.com/willisdeving) · [CodePen](https://codepen.io/addicted2crypto)

<details>
<summary>Public code & activity</summary>

[Repositories](https://github.com/addicted2crypto?tab=repositories) · [Contributions](https://github.com/addicted2crypto) · [DCGP commits](https://github.com/addicted2crypto/DCGP/commits) · [DCGP releases](https://github.com/addicted2crypto/DCGP/releases)

Browse by language: [C#](https://github.com/search?q=user%3Aaddicted2crypto+language%3AC%23&type=repositories) · [SQL](https://github.com/search?q=user%3Aaddicted2crypto+language%3ASQL&type=repositories) · [TypeScript](https://github.com/search?q=user%3Aaddicted2crypto+language%3ATypeScript&type=repositories) · [Python](https://github.com/search?q=user%3Aaddicted2crypto+language%3APython&type=repositories) · [JavaScript](https://github.com/search?q=user%3Aaddicted2crypto+language%3AJavaScript&type=repositories)

</details>
