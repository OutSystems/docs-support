---
summary: OutSystems Personal Environment is the free, cloud-based version of OutSystems. Check these FAQ to learn more.
---

# What's an OutSystems personal environment?

<div class="info" markdown="1">

We've been working on this article. Please let us know how useful this new version is by voting.

</div>

The Personal Environment (PE) is the **free, cloud-based version** of OutSystems. It allows you to create, deploy, and run your personal applications.

When you [create an account](https://www.outsystems.com/home/GetStartedForFree.aspx) at the OutSystems community, we'll invite you to create a Personal Environment. Once created, it's address and status will always be accessible at your [Plaform Home](https://www.outsystems.com/home) page.

## Is it really free? Until when?

Yes, **completely free**.

Your Personal Environment will be available:

* as long as you continue developing your apps or

* your apps are consistently accessed by end-users.

If you stop developing in your Personal Environment for an extended period of time, your Personal Environment will be recycled. This saves resources for active personal environments. But don't worry! Long before that happens, we'll let you know. We'll send you emails reminding you to continue developing in your Personal Environment.

If your environment ends up being recycled, we'll create a snapshot of the applications you had. We'll send you an email with instructions on how you can restore your apps in a new environment. Keep in mind that we only take a snapshot of the applications, not the data, and also, the snapshot will be available for the next 6 months only.

## What kind of applications can I run in a Personal Environment?

You can develop **any mobile or web application** that you can build with OutSystems. Just keep in mind that the Personal Environment is best suited for small deployments such as personal apps with dozens of users. It's not suited for mission-critical or heavy usage apps. You should consider an enterprise subscription if you are looking for higher scalability and support.

## Is there any limit on the complexity of the apps I can build?

There are **no limits** on the type, size, or complexity of applications you can build outside of those imposed by a shared environment. Personal environments are a way for you to learn, experiment, or prototype apps at your own pace.

## Is there any limit on the number of users that can access my apps?

There are **no user limits** outside of those imposed by a shared environment. In practice, this means that apps generally perform well as long as the number of concurrent users is below 100.

## What's the service level agreement (SLA) for a personal environment?

There are **no SLAs** for Personal Environments.

Apart from scheduled maintenance updates, your Personal Environment is up and running 24x7 without interruptions. But as a free offering, there are no SLAs for availability or performance.

## What kind of support is available?

Support for Personal Environments is delivered on a best-effort basis only, without any response time commitment. Developers using a Personal Environment are encouraged to rely on the [**community forums**](https://www.outsystems.com/forums/) for development support. OutSystems constantly monitors all Personal Environments for infrastructure problems, so those should be fixed automatically.

We ask that you [contact OutSystems Support](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/01_Contact_OutSystems_technical_support) only if the issue you are experiencing is infrastructure related and is still happening after a couple of hours since you first spotted it.

If you have an ongoing commercial evaluation using a Personal Environment and you hit a road block, contact our chat support. Let us know you're evaluating so we're able to provide you with the full Enterprise-grade experience.

## Can I use a personal environment to integrate with external databases or services?

Yes, you can integrate your personal environment with **publicly available web services**, and **databases**, including SQL Server, Oracle, DB2, and MySQL. VPN access is only supported for subscription customers.

OutSystems built in [SAP integration](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/SAP/Integrate_with_a_SAP_System) isn't included.

## Can I get the source code of my applications?

Detaching the source code of your applications is only available for subscription licenses.

## What are the limitations of personal environments?

* **2GB database storage:** Your Personal Environment is capable of storing up to 2GB of system and application data. Besides this OutSystems database, [you can also connect your applications to other databases](https://www.outsystems.com/evaluation-guide/use-outsystems-with-existing-databases/#3).

* **One developer per Personal Environment:** Your Personal Environment doesn't allow collaboration between several developers. You must use your OutSystems user to develop your applications.

* **One development environment:** Your Personal Environment includes one environment and it's impossible to deploy your applications to other environments.

* **Personal Environment auto-suspension:** If you stop developing or if your applications aren't being used, your Personal Environment will go to sleep. If you don't wake your environment up after an extended period of time, your applications will be saved and your Personal Environment will be recycled. Long before that happens, we'll let you know. For more information, see [here](https://success.outsystems.com/Support/Personal_Environment/What's_an_OutSystems_personal_environment%3F#Is_it_really_free.3F_Until_when.3F).

* **Shared resources:** Your Personal Environment lives in a shared cloud infrastructure where resources, such as memory and CPU are shared among several environments. This means that the performance of your applications will suffer if you exceed 100 concurrent end-users.

* **Limited version history:** By default, a new version of your application module is saved every time you publish. Module versions that are older than one week are automatically deleted.

* **No backup and restore available:** Database backups are only available for subscription licenses. It won't be possible to restore any deleted data.

* **No custom domain:** Your applications live in the [outsystemscloud.com](https://outsystemscloud.com/) domain.

* **No direct database access:** Check alternate ways on [how to extract data from your application](https://success.outsystems.com/Support/Personal_Environment/Personal_environment_hosting_infrastructure_under_the_hood#Extracting_your_data). You can't use stored procedures.

* **No VPN:** You can't request the creation of a VPN connection in your Personal Environment.

* **SaaS components:** OutSystems provides SaaS components such as, for example, [Architecture Dashboard](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Manage_technical_debt/), [Workflow Builder](https://success.outsystems.com/Documentation/Workflow_Builder) or [Experience Builder](https://success.outsystems.com/Documentation/Experience_Builder). These components may not be available for Personal Environments, at OutSystems discretion. Make sure to check the requirements in each component's documentation.

## Additional information

For more information, see [End-user license agreement](https://www.outsystems.com/legal/end-user-licensing-agreement/).

If you are evaluating OutSystems for your company and require any of the capabilities that aren't available, contact our chat support.
