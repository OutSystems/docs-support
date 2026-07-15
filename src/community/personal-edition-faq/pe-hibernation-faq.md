---
guid: b8e8a5da-3f85-4be0-b75f-e85ade6b30d4
locale: en-us
summary: OutSystems Developer Cloud (ODC) Personal Edition hibernation FAQs covering the 72-hour sleep state, wake-up steps, app behavior, and lifecycle.
figma:
coverage-type:
  - understand
topic:
app_type: reactive web apps,mobile apps
platform-version: odc
audience:
  - Developer
tags:
  - Development lifecycle
  - Lifecycle
outsystems-tools:
  - odc studio
  - odc portal
isautopublish: true
---
# Outsystems Personal Edition hibernation FAQ

**What is PE hibernation?**

Hibernation is a low-resource sleep state for OutSystems Personal Edition (PE). After 72 hours of development inactivity, your PE automatically hibernates, which means everything you've built is fully preserved, and you can wake it up whenever you need it. The PE stays free. Hibernation is what makes it sustainable to keep it that way at scale.

**When does my PE hibernate?**

Your PE enters hibernation automatically after 72 hours of inactivity. There's no manual action required, and nothing you need to do to opt in or out.

**What counts as development activity?**

Activity that prevents hibernation includes:

* Logging in to ODC Studio
* Publishing or promoting applications
* Accessing ODC Portal
* Running tests or debugging your apps
* Any developer action that requires the environment to be online

**Will I lose any work when my PE hibernates?**

No. All your code, apps, and data are preserved exactly as you left them. When you wake your PE up, you pick up right where you stopped.

**How do I wake up a hibernated PE?**

You have two self-serve options, with no forms or support tickets needed:

* Manually, from the **ODC Portal**. Open the **Manage Organization** console and wake the stage.
* Automatically, by performing a developer action that requires the environment to be online — for example, logging in or doing a **1-Click Publish** from ODC Studio.

**How long does reactivation take?**

Reactivation is fast, typically up to 2 minutes.

**Is "hibernated" the same as "deleted"?**

No. These are two different states:

* **Hibernated**: your PE is asleep but fully preserved. You can wake it up at any time.
* **Deleted**: your PE is removed. This happens only after an extended period of inactivity, as described in the PE lifecycle, and waking up doesn't reverse it.

**What happens to my published apps when my PE hibernates?**

While your PE is hibernated, end users can't access your published apps. They see a message in the browser explaining that the app is hibernated, with guidance on what to do.

As soon as you wake your PE up, your apps are available again.

**How will I know my PE is hibernated?**

You'll see a hibernation icon next to the stage in the ODC Portal consoles. Inside ODC Studio, actions that require an online environment, such as Open in Browser, Debug, Preview/Edit Data, or Test Agents, show an alert dialog if the environment is still hibernated, with a link to the **Manage Organization** page.

**Why did OutSystems introduce hibernation?**

The PE is free for prospects evaluating OutSystems and for community developers building with it. We want to keep it that way, and we want to keep expanding what you can do with it, including AI capabilities like agentic solutions and intelligent development tools. Hibernation recovers resources from inactive PEs so we can give every prospect a dedicated environment, support more community use cases, and keep the PE free at scale. It also lets us be more generous with the overall PE lifecycle. Developers get more room between sessions before a PE is removed for inactivity.

**Will my PE still be deleted if I don't use it?**

The PE lifecycle still applies. PEs that remain inactive for an extended period are eventually removed. Hibernation doesn't replace deletion. It sits between active use and deletion, giving you a longer window to come back. Waking your PE up resets the inactivity clock.

**Does hibernation cost anything?**

No. The PE is free, and hibernation does not change that.
