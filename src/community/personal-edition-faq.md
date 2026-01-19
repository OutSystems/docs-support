---
guid: 2f0b4814-c8d5-41be-a9bf-c0a15b5cc917
locale: en-us
summary: Frequently asked questions about OutSystems Personal Edition
figma: 
coverage-type: 
topic: 
app_type: reactive web apps,mobile apps
platform-version: odc
audience: 
tags: 
outsystems-tools: 
---

# OutSystems Personal Edition FAQ

**What is the OutSystems Personal Edition, and who can use it?**

The OutSystems Personal Edition (also referred to as PE) is the new, free version of OutSystems Developer Cloud (ODC), designed for all users, including prospects, customers, partners, and community members. Its primary purpose is to provide a dedicated space for exploring the platform, learning, and contributing to the OutSystems ecosystem. Anyone with a Community Account can request the OutSystems Personal Edition.

**Is the OutSystems Personal Edition free and forever?**

The OutSystems Personal Edition is free of charge and can be retained indefinitely as long as you continue to use it.

* Whenever you register for a new Personal Edition, you must log in within the first three days. If you don’t do so, you will need to request a new one.

* You need to use it regularly; if not, the Personal Edition will be deleted, and you will permanently lose all your progress, configurations, and data. To avoid losing your work, export your apps’ OML files before deletion. This allows you to save your apps locally and import them into a new Personal Edition at a later time.

* Even if your current Personal Edition gets deleted, you can always request a new one. To do it, you must go to the [Personal Edition](https://www.outsystems.com/personaledition/) portal and request a new one.

**I've requested a Personal Edition, but it's not yet available. What happened?**

Personal Editions are usually available right away. In rare cases, high demand might mean your Personal Edition takes longer to create, and you'll be placed on a waiting list. Creation times vary, we'll email you as soon as your Personal Edition is ready.

**Can I invite my team to access my OutSystems Personal Edition?**

Yes. The invite is done from the ODC portal, and users will access the ODC portal from the invitation email. If they are already Community users, they will input their Community credentials and access OutSystems. If not, they will be redirected to the sign-up form before accessing the ODC portal.

**What is included in the OutSystems Personal Edition?**

The OutSystems Personal Edition is designed for training, sandboxing, and exploring ODC, and it is thus different from the commercial-grade ODC tenant we provide our customers and includes the following:

* 1 Development stage

* 2 API clients

* Up to 100 internal users

* Up to 8 active components running at any given time. This total includes applications, workflows, AI agents, and timers.
  For example, your OutSystems Personal Edition can run 3 applications, 2 workflows, 2 AI agents, and 1 timer simultaneously.

* Up to 1GB of database storage

* Up to 10 min/day of custom code execution

* Up to 30 min/day of timer execution

* Up to 10 min/day of external libraries execution

* Up to 50 application logs/minute

All the above limits are controlled on the [subscription console](https://www.outsystems.com/tk/redirect?g=504cdfa5-68d4-46ce-8363-e08aa05e4514).

**Can I use add-ons in my Personal Edition?**

Add-ons are not included in the Personal Edition, except for Private Gateways.

**What kind of apps can be built in the OutSystems Personal Edition?**

The OutSystems Personal Edition can be used to develop any type of OutSystems application, from mobile to web, agentic apps, and workflows.
Note that OutSystems Personal Editions are designed for exploration, training, and sandboxing use cases, so they are best suited for small developments. It's not supported for mission-critical or heavy-usage apps.

**Is the Agent Workbench available in OutSystems Personal Edition?**

Yes, Agent Workbench is available for free for everyone in the OutSystems Personal Edition. We encourage everyone to take advantage of it.

**Are AI trial models available in the OutSystems Personal Edition?**

Yes. Trial models, Claude 3.7 Sonnet, and Amazon Nova Pro are supported by default in OutSystems Personal Edition to help prospects test Agent Workbench without needing their own AI models.  These trial AI Models have the following fixed usage limits and cannot be renewed:

* Request Limits per Tenant: 1000

* Request Limits per Tenant per Minute: 20

* Token Limits per Tenant per min: 100k

* Token Limit per Tenant: 4M

**What happens when I reach the limit of my Trial model when using an Agent?**

Once the limit is reached, additional calls return an error. In the ODC Portal's AI models console, the trial card shows that the limit has been reached.
Passing the error information to the agent's end user depends on your design of the Agentic app, but the event is always logged and shown in the ODC Portal, on the Logs page.

As described above, AI trial models cannot be renewed.  If you have your own paid AI models, you can add them to your OutSystems Personal Edition.

**Is Mentor available in the OutSystems Personal Edition?**

Yes. Mentor is available in Personal Edition with the known [usage restrictions](https://www.outsystems.com/tk/redirect?g=D940C32D-0409-4D49-B6FE-BB831E5EF12C).

**Can the Personal Edition be used to integrate with external databases or services?**

Yes. Extensibility is available in the OutSystems Personal Edition. The OutSystems Personal Edition includes the Private Gateway add-on, which allows you to connect to your own private external databases and services.

**Can I connect my OutSystems Personal Edition to my external  Identity Provider (IdP)?**

Yes, at the Applicational level. You can use your external IdP in your applications, but you cannot use it to log in to the OutSystems Personal Edition. To use your external IdP, you need to configure it on the ODC Portal. To log in to the OutSystems Personal Edition, you will always need to use your Community account..

**Can I use external Static Application Security Testing (SAST) analysis tools on my Personal Edition apps?**

No. Integration with SAST tools is not available on Personal Editions.

**Can I deploy my OutSystems Personal Edition application to the Production stage?**

No. The OutSystems Personal Edition is limited to one stage, the Development stage.

**Is there any limit on the number of users who can access the apps built with the Personal Edition?**

Yes. Up to 100 users; however, we don’t recommend exceeding dozens of users since these tenants are not ready for production loads, and the experience will be affected.

**Are we retiring O11 Personal Edition?**

No. OutSystems 11 Personal Edition continues to exist, and you can still use it for O11 training and O11 Forge community use cases. The OutSystems 11 Personal Edition is accessible in the Community menu, Tools > O11.

**Can a user have both the OutSystems Personal Edition and the OutSystems 11 Personal Edition?**

Yes, a user can have both Personal Editions.

**Can a prospect migrate their apps from O11 Personal Edition to OutSystems Personal Edition?**

No. A direct app upgrade path from an O11 Personal Environment to OutSystems Personal Edition does not exist.

**Can a user move their apps from one OutSystems Personal Edition to another OutSystems Personal Edition?**

Yes. Although no direct migration between OutSystems Personal Editions is in place, you can export and import your apps from one OutSystems Personal Edition to another. Note that configurations and applicational data will be lost.

**What's the service level agreement (SLA) for the OutSystems Personal Edition?**

There aren’t SLAs for OutSystems Personal Editions. The OutSystems Personal Edition is set to be up and running 24x7 without interruptions. However, as a free offering, there are no SLAs for availability or performance.

**What kind of support is available?**

Support for OutSystems Personal Edition is provided; you can open a support ticket via the ODC Portal. Also, Community members can access other supporting resources, such as [ODC documentation](https://success.outsystems.com/documentation/outsystems_developer_cloud/), [online training](https://learn.outsystems.com/training?_gl=1*10dgdh9*_gcl_aw*R0NMLjE3NTc0MDgzMDUuQ2owS0NRandvUF9GQmhERkFSSXNBTlBHMjRPM1lLVURlUzdsTlJxNXdNMmlKcXNSeFlnUEFpbzlxWE9SWk1tcmZONWMwY1l2Z2NkWnBja2FBcFFQRUFMd193Y0I.*_gcl_au*MzgyNjc2NjQxLjE3NTE1MzcyODIuNzczMzc0NDUuMTc1ODAyNjI5MS4xNzU4MDI2Mjkx*_ga*ODg2NDg1NzgxLjE2NzE2MzI4NjA.*_ga_ZD4DTMHWR2*czE3NTg3OTAxMDUkbzE0OCRnMSR0MTc1ODc5Mzc5NyRqNjAkbDAkaDA.*_ga_HGKNZZMWJS*czE3NTg3OTAxMDYkbzQ3NSRnMSR0MTc1ODc5Mzc5NyRqNjAkbDEkaDE4OTU5NDcyOTI.*_ga_G11QMS1MBT*czE3NTg3OTAxMDUkbzMkZzEkdDE3NTg3OTM3OTckajYwJGwwJGgw), [community support](intro.md), and [AI-powered assistance](https://www.outsystems.com/DSUP_AI_UI/AISearchAgent?Search=). If you need help evaluating how OutSystems can address your app challenges today, [talk to us](https://www.outsystems.com/schedule-demo/) or check our [Evaluation Guide](https://www.outsystems.com/evaluation-guide/).

**Is it possible to contribute to ODC Forge in a Personal Edition?**

Yes. The new Personal Edition makes it easier for every developer to contribute and collaborate on the Forge. By making it easier for the community to contribute, OutSystems can scale the number of AI Agents available to customers. This helps accelerate the adoption of the AI Agent Workbench and provides customers with a wider variety of ready-to-use solutions.

**Can I upload assets to Forge in my individual name?**

Yes. You can use your OutSystems Personal Edition to submit assets to ODC Forge. Assets submitted this way will be attached to your Personal Edition. The displayed publisher name in ODC Forge will be the **First and Last Name** of your Community Account..

**Can I have other Community members collaborating on my ODC Forge assets?**

Yes. You’ll be able to invite other team members to your own Personal Edition. This allows others to make changes to your assets and submit new versions of them to ODC Forge.

**Will my Forge assets contribute to my Community Profile ranking?**

Yes. Not immediately at the ONE Conference. However, the Developer Relations team is planning to ensure that ODC Forge assets will count towards your community profile ranking in the future. Importantly, any points you’ve already earned from Forge assets will also be taken into account when this is rolled out.

**Can I transfer the Forge assets I uploaded in my Company’s tenant to my OutSystems Personal Edition?**

There won’t be an automated process to ensure this. After having submitted a first asset through their OutSystems Personal Edition to Forge, users from the Community should request this by Support Case, with proof that their Company acknowledges the ownership transfer of the Forge asset.
