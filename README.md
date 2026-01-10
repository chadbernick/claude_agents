

````markdown
# Claude Code Agents

A curated library of **Claude Code subagents** – reusable, role-based AI agents designed to support everything from low-level coding and infrastructure to research, product strategy, and executive-level communication.

Each top-level folder represents a **track** of related agents. You can mix and match them to build full end-to-end workflows inside Claude Code.

---

## Goals

This repository exists to:

- Capture **repeatable roles** you actually use (not one-off prompts).
- Encode **domain expertise** (PE, cloud, AI, infra, exec strategy, etc.) into agents.
- Enable **composable workflows** – research → design → implementation → QA → narrative – without redefining expectations every session.
- Make it easy to **fork and adapt** agents to your own organization, stack, and constraints.

---

## Using These Agents in Claude Code

Claude Code supports both **project-specific** and **global/user** agents.

### Project-Specific Agents (recommended)

Project agents live inside a repo/workspace and are scoped to that project.

1. In your project, create a local agents directory:

   ```bash
   mkdir -p .claude/agents
````

2. Copy any agents you want from this repo into that directory, for example:

   ```bash
   cp 01-core-development/* .claude/agents/
   cp 05-data-ai/* .claude/agents/
   cp 11-executive-strategy/* .claude/agents/
   ```

3. Open the project in Claude Code (or reload it).
   The agents will appear in the Claude Code agents panel for that project.

> **Precedence:**
> If an agent with the same name exists both in the project and globally, the **project-specific** one wins.

### Global/User Agents

Global agents are available across all projects on your machine.

1. Create a global agents directory (if it doesn’t exist):

   ```bash
   mkdir -p ~/.claude/agents
   ```

2. Copy agents you want to use everywhere:

   ```bash
   cp 01-core-development/* ~/.claude/agents/
   cp 06-developer-experience/* ~/.claude/agents/
   ```

> **Precedence:**
> Global agents are used when there is **no** project-specific agent with the same name.

---

## Repository Structure

Each folder groups agents by their primary focus:

* **`01-core-development/`**
  Generalist and specialist development agents (implementation, refactoring, debugging, code review).

* **`02-language-specialists/`**
  Agents tuned for writing and editing: documentation, specs, narratives, blog posts, and other written artifacts.

* **`03-infrastructure/`**
  Cloud and platform agents: infrastructure-as-code, architecture reviews, CI/CD pipelines, migration patterns.

* **`04-quality-security/`**
  Testing and security agents: unit/integration test generation, defensive coding review, basic threat modeling.

* **`05-data-ai/`**
  Data and AI agents: data modeling, analytics, RAG patterns, MLOps, AI/ML architecture for real products.

* **`06-developer-experience/`**
  Developer experience, docs, onboarding, runbooks, and workflow ergonomics.

* **`07-specialized-domains/`**
  Domain-specific agents (e.g., healthcare, manufacturing, capital markets, NGOs, etc.) tuned with sector-aware language and concerns.

* **`08-business-product/`**
  Product and business agents: outcome-based planning, PRDs, customer journeys, value propositions, and GTM narratives.

* **`09-orchestration/`**
  “Conductor” agents that coordinate other subagents or help you design multi-step workflows.

* **`10-research/`**
  Research, analysis, and synthesis agents: market analysis, competitive intel, and turning noisy input into structured insight.

* **`11-executive-strategy/`**
  Executive and board-facing agents: strategy memos, portfolio value creation narratives, mutual action plans, and C-suite communication.

---

## How Agents Are Structured

Individual agents vary, but most follow a consistent pattern inspired by the **executive-strategy** track:

* **Role & Persona**
  A clear “who am I?” statement (e.g., *“Private Equity Operating Partner for Cloud & AI Value Creation”*).

* **Scope & Responsibilities**
  The boundaries of the role: what the agent owns and what it must not do.

* **When to Use This Agent**
  Situations where this agent is the right tool (and common anti-patterns where it isn’t).

* **Inputs**
  The minimum context you should provide: code, architecture diagrams (described in text), business objectives, constraints, KPIs, etc.

* **Outputs**
  Expected deliverables: code diffs, design docs, checklists, architecture narratives, mutual action plans, executive briefings, etc.

* **Guardrails**
  Things to explicitly avoid (e.g., fabricating financial numbers, rewriting production interfaces, ignoring regulatory constraints).

This structure makes agents easy to **compose** without stepping on each other’s toes.

---

## Example Workflows

### 1. Shipping a Feature End-to-End

1. **Research:** Use a `10-research` agent to map user needs and competitive context.
2. **Product:** Use an `08-business-product` agent to draft a concise PRD or outcome brief.
3. **Build:** Use a `01-core-development` agent to implement and refactor the feature.
4. **Quality & Security:** Use `04-quality-security` agents for tests, validation, and basic threat modeling.
5. **Docs & DX:** Use `06-developer-experience` agents to update docs, READMEs, onboarding guides, and changelogs.

### 2. Data & AI Modernization for a Portfolio Company

1. **Research:** Use `10-research` to summarize market and technology trends relevant to the portfolio company.
2. **Data & AI:** Use `05-data-ai` to design a data/AI architecture (RAG, analytics, ML, etc.).
3. **Infrastructure:** Use `03-infrastructure` to propose target cloud and platform designs.
4. **Business Outcomes:** Use `08-business-product` to articulate business outcomes and KPIs.
5. **Executive Narrative:** Use `11-executive-strategy` to produce an exec-ready memo, board update, or mutual action plan.

### 3. Hardening an Existing System

1. **Infrastructure:** Use `03-infrastructure` to assess and modernize architecture, IaC, and CI/CD.
2. **Quality & Security:** Use `04-quality-security` agents for testing, security review, and guardrails.
3. **DX & Documentation:** Use `06-developer-experience` to produce runbooks, incident guides, and onboarding docs.

---

## Customizing for Your Organization

You are expected to **fork and adapt** these agents:

* Rename roles to match your org (e.g., *“Platform Engineering Lead”*, *“CPO”*, *“Operating Partner – Data & AI”*).
* Encode real constraints: tech stack (AWS/GCP/Azure), regulatory context, data residency, SLAs, budgets.
* Align outputs with your internal templates: OKRs, outcome-based management, board memo formats, or PR/FAQ style docs.
* Tighten or relax guardrails depending on where the agent is used (exploration vs. production workstreams).

A practical pattern:

1. Start with an agent from this repo that’s closest to what you need.
2. Copy it into your project’s `.claude/agents/` directory.
3. Tune the persona, inputs/outputs, and guardrails based on real work you’re doing.
4. Iterate – treat agents as living tools, not static prompts.

---

## Suggested Starter Set

If you want a small but powerful starting lineup:

* 1–2 **core dev** agents from `01-core-development/`
* 1 **infra/platform** agent from `03-infrastructure/`
* 1 **quality/security** agent from `04-quality-security/`
* 1 **data/AI** agent from `05-data-ai/`
* 1 **product/business** agent from `08-business-product/`
* 1 **executive strategy** agent from `11-executive-strategy/`

This covers the full chain: **code → infra → quality → data/AI → product → executive narrative**.

---

## Contributing

If you:

* Have a new agent pattern that works well,
* Want to extend these to new domains,
* Or see ways to improve the structure and guardrails,

feel free to open an issue or a pull request with your proposed changes.

```

You can paste this over the current root `README.md` and tweak language or sections (e.g., add more domain-specific examples) as you refine the agents.
::contentReference[oaicite:0]{index=0}
```
