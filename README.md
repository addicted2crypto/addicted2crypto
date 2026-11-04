<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/hero-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="./assets/hero-light.svg" />
  <img src="./assets/hero-light.svg" alt="Will · addicted2crypto. AI systems, data research, and full-stack engineering. C#, SQL, TypeScript, Python, JavaScript, and .NET." width="100%" />
</picture>

<p align="center">
  <a href="https://williamsforeverportfolio.vercel.app"><strong>Explore my work ↗</strong></a> ·
  <a href="https://onchaintruth.xyz"><strong>Live applications ↗</strong></a> ·
  <a href="https://linkedin.com/in/william360"><strong>Let's connect ↗</strong></a>
</p>

I'm **Will**, an AI and full-stack engineer with **8+ years shipping production systems**. I build C#/.NET services, SQL-backed data pipelines, local model orchestration, and typed web applications. My work spans federal health IT, developer tooling, and on-chain research.

**Start with the work:** [AI systems](#the-local-ai-stack) · [Live products](#live-products) · [How I engineer](#under-the-hood) · [Activity](#engineering-activity)

---

## The local AI stack

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/stack-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="./assets/stack-light.svg" />
  <img src="./assets/stack-light.svg" alt="DCGP governs context; WillAgent orchestrates models and tools; EVMSleuth applies the stack to on-chain analysis." width="100%" />
</picture>

### [DCGP ↗](https://github.com/addicted2crypto/DCGP)

**Context governance for agentic development.** Typed boundaries, policy gates, and tooling that make context handling explicit across an AI development workflow.

[Read the source](https://github.com/addicted2crypto/DCGP) · [Explore releases](https://github.com/addicted2crypto/DCGP/releases) · [See the onboarding guide](https://github.com/addicted2crypto/DCGP#installation)

<details>
<summary><strong>Inspect the engineering: governance, integrations, and failure boundaries</strong></summary>

- **Boundaries:** explicit project context, typed configuration, and schema validation.
- **Interfaces:** CLI, MCP, editor integrations, and an opencode plugin.
- **Review path:** start with the repository's configuration examples, then follow how a policy becomes an output gate.
- **Evaluation question:** which classes of invalid output are detected, and what happens when a gate rejects a result?

[Open the project documentation](https://github.com/addicted2crypto/DCGP#readme)

</details>

### [WillAgent ↗](https://github.com/addicted2crypto/willagent)

**Local model orchestration with explicit control.** A typed tool layer, persistent state, local/cloud model routing, termination controls, and audit logging.

`NestJS` · `TypeScript` · `Redis` · `Docker` · `Ollama`

[Inspect the source](https://github.com/addicted2crypto/willagent) · [Read the project guide](https://github.com/addicted2crypto/willagent#readme)

<details>
<summary><strong>Trace a run: context → model → tool → evidence</strong></summary>

The system separates four responsibilities:

1. Establish the task's context and constraints.
2. Route the request between local inference and a cloud model.
3. Execute registered tools with typed inputs and persistent state.
4. Record actions and results so failures can be inspected.

The questions I care about: **Which model ran? Which tools executed? What evidence supports the result? Can the run be stopped and inspected?**

[Follow the implementation](https://github.com/addicted2crypto/willagent)

</details>

### EVMSleuth

**The application layer.** Contract analysis, wallet tracking, and token research built around the local AI stack. Private repository.

`NestJS` · `TypeScript` · `PostgreSQL` · `Redis` · `BullMQ`

Public examples of my data-product work: [onchaintruth.xyz](https://onchaintruth.xyz) · [hCASH](https://hcash.onchaintruth.xyz) · [Moat](https://moat.onchaintruth.xyz/leaderboard)

---

## Live products

| Open it | What to inspect | Engineering behind it |
| --- | --- | --- |
| **[onchaintruth.xyz ↗](https://onchaintruth.xyz)** | Portfolio cost basis and performance against USD and BTC | Typed application layer, on-chain reads, data modeling |
| **[hCASH ROI Oracle ↗](https://hcash.onchaintruth.xyz)** | Mining ROI, break-even thresholds, and scenario projections | Price oracles, API integration, scheduled data collection |
| **[Moat OCA Leaderboard ↗](https://moat.onchaintruth.xyz/leaderboard)** | Strategy performance against AVAX and BTC benchmarks | Live reserve reads, opportunity-cost modeling, portfolio analytics |

**Also building:** GymTech, a multi-tenant platform for martial arts and fitness gyms, with role-based access, subscriptions, Stripe Connect, and QR check-in.

## Recently shipped

<!-- SHIPPED:START -->
[DCGP releases](https://github.com/addicted2crypto/DCGP/releases) · [WillAgent releases](https://github.com/addicted2crypto/willagent/releases)
<!-- SHIPPED:END -->

---

## Engineering activity

<!-- TELEMETRY:START -->
<p align="center">
  <img src="https://github-stats-extended.vercel.app/api?username=addicted2crypto&amp;theme=dark_github&amp;hide_border=true&amp;hide_rank=true&amp;contribs_include_own_repos=true&amp;include_all_commits=true&amp;show_icons=true&amp;show=reviews,prs_merged&amp;number_format=long&amp;disable_animations=true" alt="GitHub activity, including owned repositories, reviews, and merged pull requests. Different fields use different time windows." />
</p>
<!-- TELEMETRY:END -->

[Inspect my contribution calendar](https://github.com/addicted2crypto?tab=overview)

<details>
<summary>More activity: contribution streak and repository languages</summary>

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=addicted2crypto&amp;theme=github-dark-blue&amp;hide_border=true&amp;disable_animations=true&amp;timezone=America%2FLos_Angeles" alt="Daily contribution streak and lifetime contribution total" width="49%" />
  <img src="https://github-stats-extended.vercel.app/api/top-langs/?username=addicted2crypto&amp;theme=dark_github&amp;layout=compact&amp;langs_count=6&amp;hide_border=true&amp;disable_animations=true" alt="Repository language distribution by code size" width="49%" />
</p>

<sub>Cards refresh periodically and use different date windows. Language percentages describe repository code size. Public services have limited visibility into private work.</sub>

</details>

<!-- SNAKE:START -->
<!-- The optional workflow inserts a contribution animation here after it successfully generates the assets. -->
<!-- SNAKE:END -->

---

## Under the hood

<details>
<summary><strong>AI systems: context, routing, execution, and auditability</strong></summary>

I build local inference and cloud API workflows with explicit routing, registered tools, context boundaries, and persistent state. The interesting work is in failure handling: validating inputs, gating outputs, terminating execution, and preserving evidence.

**Stack:** Ollama · Claude API · MCP · NestJS · Redis · BullMQ

</details>

<details>
<summary><strong>Full-stack systems: typed boundaries and data that stays useful</strong></summary>

C#/.NET and NestJS/Node.js services, Next.js interfaces, SQL and PostgreSQL, Redis, and scheduled pipelines. My applications connect ingestion, research, modeling, background jobs, and user-facing decisions.

**Stack:** C# · .NET · ASP.NET MVC · SQL · TypeScript · Python · Next.js · PostgreSQL · Supabase · Docker · Azure

</details>

<details>
<summary><strong>Security and federal health IT</strong></summary>

DoD contract engineering supporting DHA.mil, with experience in Sitecore, ASP.NET MVC, Docker-based development, Section 508, and CAC/AD FS integration.

**Background:** CompTIA Security+ · IAT II · DoD-cleared

I bring that experience to AI and application work through explicit permissions, validation, evidence requirements, and audit logging.

</details>

## Work with me

Interested in **AI systems, developer infrastructure, or full-stack products**? Start with a project above, then send me the problem you're working on.

**[LinkedIn ↗](https://linkedin.com/in/william360)** · [Portfolio](https://williamsforeverportfolio.vercel.app) · [X / @willisdeving](https://twitter.com/willisdeving) · [CodePen](https://codepen.io/addicted2crypto)
