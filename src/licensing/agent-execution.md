---
summary: 
tags: 
locale: en-us
guid: 9fafc3bd-31db-46b9-99a5-36d7aaaaebc8
app_type: traditional web apps,mobile apps,reactive web apps
helpids:
platform-version: o11,odc
figma: https://www.figma.com/design/MMGFR5F26En9lwH0EhScIX/TK-Design---Stuff?node-id=6346-1078&t=ljzgyYbhWZE6lAKB-1
audience:
  - mobile developers
  - frontend developers
  - full stack developers
  - tech leads
  - architects
outsystems-tools:
  - service studio
  - odc studio
  - odc portal
  - service center
coverage-type:
  - understand
topic:
---

# Agent execution

An Agent Execution is counted each time the action CallAgent is executed in runtime. Independent of how many actions or tools the Agent is using or how many times it calls an AI model inside that loop, each call to the Agent is still only 1 Execution. The following diagram shows a detailed example of how Agent executions and AOs are counted:

![Diagram showing how Agent executions and AOs are counted, including API call, Timer, App, Workflow, Orchestrator Agent, AI Model GPT5, Intake Agent, Communicator Agent, AI Model Claude4, and actions.](images/agent-ao-usage-diag.png "Agent Execution and AO Usage Diagram")
