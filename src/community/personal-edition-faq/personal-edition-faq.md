---
guid: 2f0b4814-c8d5-41be-a9bf-c0a15b5cc917
locale: en-us
summary: OutSystems Developer Cloud (ODC) Personal Edition FAQ covering features, usage limits, AI trial models, Forge contributions, and support.
figma:
coverage-type:
  - remember
  - understand
topic:
  - pe-expiration-policy
  - pe-hibernation-basics
  - pe-resource-limits
app_type: reactive web apps,mobile apps
platform-version: odc
audience:
  - Developer
tags:
  - Agentic
  - AI
  - Forge
  - Lifecycle
  - Mentor
  - Mentor Studio
  - Private Gateway
outsystems-tools:
  - odc portal
isautopublish: true
---

# OutSystems Personal Edition FAQ

## At a glance

| Topic | Detail |
| --- | --- |
| Price | Free, no credit card required |
| How long does it last? | Active for 15 days by default, and it stays active while you build and govern |
| AI | Conversational development (Mentor) and agent orchestration (Agent Workbench) included. Mentor: 11.5M tokens per day, also used through MCP |
| Users | Up to 100 internal users |
| Stages | Development only; production isn't included |
| Support | Best effort, no Service-Level Agreement (SLA) |
| Can I move to a paid edition? | [Contact us](https://www.outsystems.com/). You can export your apps and agents to take them with you. |

## Can I build and govern apps and AI agents for free with OutSystems?

Yes. OutSystems Personal Edition is free and requires no credit card. Everything you build web apps, mobile apps, AI agents, and agentic workflows is built within your own governed portfolio, under your own rules, guardrails, and architecture. Nothing is built outside it. Create through conversational development (Mentor), orchestrate agents that work together (Agent Workbench), and connect to your existing systems and data (Private Gateway). Governance is applied from the first prompt, so what you prototype stays secure and consistent as it grows. Personal Edition is for evaluating, learning, development, and testing, not production.

Personal Edition also suits personal apps and hobby projects. Your free environment stays active while you keep building.

## Can I use Claude Code or other AI coding assistants to build and govern OutSystems apps and agents?

Yes. Supported AI tools such as Claude Code, Cursor, or AWS Kiro, or any tool compatible with the Model Context Protocol (MCP) can connect to OutSystems MCP to read, build, and govern apps and agents in your Personal Edition. Start by requesting a Personal Edition, then follow the [OutSystems MCP setup guide](https://success.outsystems.com/documentation/outsystems_developer_cloud/agentic_development/outsystems_mcp/get_started_with_outsystems_mcp/).

## Does using OutSystems MCP use my Mentor tokens?

Yes. Each Personal Edition includes 11.5M Mentor tokens per day, shared across all the ways you use Mentor: in Mentor, Mentor Studio, and through OutSystems MCP. When your AI coding assistant (such as Claude Code, Cursor, or AWS Kiro) asks Mentor to build or change apps through MCP, that usage counts toward the same daily allowance. Your AI assistant’s own model usage, for example, your Claude Code plan, is billed separately by that provider.

## Can I prototype enterprise apps and AI agents for free?

Yes. Create your first agentic system and prototype end-to-end business apps, AI agents, and workflows connected to your own systems. Personal Edition isn't meant for production, but it's the fastest way to explore and evaluate OutSystems: build your proofs of concept, then share them with up to 100 colleagues and business stakeholders in your organization before you decide what comes next.

Start today: request a Personal Edition with no credit card, connect your AI tools, and turn an idea into a working prototype. [Request your Personal Edition.](https://www.outsystems.com/personaledition/)

## What is Personal Edition, and who is it for?

Personal Edition (PE) is a free OutSystems Developer Cloud (ODC) environment for learning, evaluating, building, and prototyping on the platform. Anyone with an OutSystems account can request one. It includes conversational development (Mentor) and agent orchestration (Agent Workbench), lets you connect to your existing systems and data (Private Gateway), and needs no credit card.

* **Price**:
    * Free, no credit card required, and free for as long as you keep building with it.
* **Team access**:
    * Invite up to 100 internal users.
* **Best for**:
    * Learning ODC, training, sandboxing ideas, and contributing to the Forge.
    * Build and govern proofs of concept and explore ideas before you commit.
    * Connect to your own external databases and services through the Private Gateway, which is included.
* **Not included**:
    * Production stage. The free Personal Edition has a Development stage only. For mission-critical apps and agents, ODC is built for production; [contact us](https://www.outsystems.com/) to plan the move.

## How do I get started?

Request a Personal Edition after logging in or signing up on the [Personal Edition page](https://www.outsystems.com/personaledition/). During high demand, you can be placed on a waiting list, and OutSystems emails you as soon as it's ready.

## Can I invite my team?

Yes. To collaborate with teammates or share what you've built, invite them from the ODC Portal. They sign in with their credentials, or create an account if they don't have one.

## What can I build?

You can build and govern any type of application: web, mobile, agentic apps, and workflows. Each Personal Edition includes these resources:

| Resource | Included |
| --- | --- |
| Development stage | 1 |
| API clients | 2 |
| Internal users | Up to 100 |
| Active components at one time | Up to 8, for example 3 apps, 2 workflows, 2 AI agents, and 1 timer |
| Database storage | 1 GB |
| Custom code execution | 10 min per day |
| Timer execution | 30 min per day |
| External libraries | 10 min per day |
| Application logs | 50 per minute |
| Private Gateway | Included |

Track your consumption in the [subscription console](https://www.outsystems.com/tk/redirect?g=504cdfa5-68d4-46ce-8363-e08aa05e4514). When you need more, paid ODC adds production stages, more capacity, and add-ons such as self-hosting and higher uptime on top of these baseline features. [Contact us](https://www.outsystems.com/) to plan your move.

## Which AI features are included?

The following table lists the AI capabilities in Personal Edition and their limits.

| Capability | What it does | Limits in Personal Edition |
| --- | --- | --- |
| Mentor | Generates new apps from a prompt | 11.5M tokens per day, refreshed daily and shared with Mentor Studio and MCP. Covers everything you build with Mentor: web and mobile apps, AI agents, and agentic workflows. Up to 20 apps generated per day, 2 per minute. [Mentor limits](https://www.outsystems.com/tk/redirect?g=D940C32D-0409-4D49-B6FE-BB831E5EF12C) |
| Mentor Studio | Changes existing apps (logic, screens, data) through conversation in ODC Studio | Shares the same 11.5M daily tokens. [AI development in Mentor Studio](https://www.outsystems.com/tk/redirect?g=27f4f846-5c2d-44fd-b9a2-99f5d2770cb2) |
| Through MCP (Claude Code, Cursor, AWS Kiro, or any MCP-compatible tool) | Asks Mentor to build or change apps from your AI coding tool | Shares the same 11.5M daily tokens. Your AI tool's own model usage is billed separately by that provider. [OutSystems MCP setup guide](https://success.outsystems.com/documentation/outsystems_developer_cloud/agentic_development/outsystems_mcp/get_started_with_outsystems_mcp/) |
| Agent Workbench trial models | Run the AI agents you build, without connecting your own model | Claude 3.7 Sonnet and Amazon Nova Pro: 4M tokens and 1,000 requests in total per Personal Edition, **not renewable**. 20 requests and 100k tokens per minute. Connect your own model to keep going. |

Mentor usage counts toward the same 11.5M-token daily allowance whether you use it in Mentor, Mentor Studio, or through OutSystems MCP. The Agent Workbench trial-model tokens are a separate allowance; using one doesn’t use up the other.

For reference, 11.5M tokens per day is enough to build a medium-sized app, such as an internal business app with 10 to 20 screens, multiple entities, and integrations with external systems, and keep iterating on it the same day.

Agent Workbench is included for everyone at no cost. You can connect your own AI models at any time.

## Is Personal Edition free, and how long does it last?

Your Personal Edition stays free and active while you keep building with it. A new Personal Edition is active for 15 days by default.

* If you use it during the last 5 days of that period, it extends automatically by 7 days, and keeps extending while you stay active.
* After 72 hours without activity, it enters [hibernation](https://www.outsystems.com/tk/redirect?g=b8e8a5da-3f85-4be0-b75f-e85ade6b30d4). Your work is saved. To wake it, use **Manage Organization** in the ODC Portal, or run any developer action, such as logging in to ODC Studio or publishing an app.
* If there's no activity by the end of the period, it's deleted. OutSystems emails you 3 days before.
* To keep your work, export your apps and agents and import them into a new Personal Edition. Only the apps move; configurations and application data are lost. You can request a new [Personal Edition](https://www.outsystems.com/personaledition/) at any time.

## Can I connect external systems, use my own identity provider, or deploy to production?

* **External databases and services**: Connect through Private Gateway, which reaches your own private external systems.
* **Identity**: Connect your external identity provider (IdP) to your applications. The ODC Portal itself stays on your Community account login.
* **Deployment**: Personal Edition has one development stage. It's built for development and testing, not production.
* **Security scanning**: External Static Application Security Testing (SAST) tools aren't available in Personal Edition.

## What support is included?

Get help from [ODC documentation](https://success.outsystems.com/documentation/outsystems_developer_cloud/), [online training](https://learn.outsystems.com/training), the [Community forums](https://www.outsystems.com/forums), and [AI-powered assistance](https://www.outsystems.com/DSUP_AI_UI/AISearchAgent). You can also open a support ticket in the ODC Portal. Support for Personal Edition is provided on a best-effort basis and has no SLA.

## Can I use pre-built components to build faster?

Yes. Start from pre-built components, connectors and agents (Forge) instead of building everything from scratch. [Browse the Forge](https://www.outsystems.com/forge/).

You can also contribute your own assets from your Personal Edition. Upload them under your name and invite other Community members to collaborate. Forge assets will count toward your Community profile ranking soon, and points you have already earned will be included.

Forge has more than 8,800 assets available, and the number keeps growing.

## How does Personal Edition compare with paid ODC?

Personal Edition is free. When you outgrow it, contact us to discuss your move to ODC. There's no self-serve upgrade path to an ODC tenant. You can export the apps and agents you have built in your Personal Edition and take them with you.

| | Personal Edition | ODC (paid) |
| --- | --- | --- |
| Price | Free, no credit card required | Get an estimate, based on application objects, end users, and add-ons |
| Runtimes | Development | Development, test, and production |
| Hosting | OutSystems Cloud | OutSystems Cloud, or self-hosted as an add-on |
| Uptime guarantee | None | 99.5%, or 99.95% as an add-on |
| Compliance | None | ISO 27001 (limited), more with add-ons |
| Users | Up to 100 internal users | Starts with 100 internal users, add internal and external users |
| Applications | Proof-of-concept applications | Starts with 1 medium production app, scale with add-ons |

## Can I move my apps and agents to another edition?

* **Between Personal Editions**: Export your apps and import them into a new one. Configurations and application data are lost, so export and import moves only the apps.
* **From OutSystems 11 Personal Edition**: There's no direct migration path. OutSystems 11 Personal Edition is still available from the Community menu.
* **Both can coexist**: You can use an ODC Personal Edition and an OutSystems 11 Personal Edition at the same time.
* **Forge assets from a company tenant**: A transfer to your Personal Edition needs a support case with proof that your company acknowledges the transfer.
