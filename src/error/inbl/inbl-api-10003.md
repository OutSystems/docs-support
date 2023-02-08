---
summary: Recommended action for the error: "Integration Manager couldn't be reached. This could be due to a network error, Integration Manager isn't present in the environment, or it's very outdated. <NetworkError>" in Integration Builder
tags:
locale: en-us
guid: 46eae534-9de4-417f-83e8-566eaa6fd946
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# OS-INBL-API-10003

## Error message

`Integration Manager couldn't be reached. This could be due to a network error, Integration Manager isn't present in the environment, or it's very outdated. <NetworkError>"`

## Cause

Integration Builder was unable to contact the Integration Manager API in your environment.

## Impact

Integration Builder isn't able to contact Integration Manager in your environment. This means that you won't be able to navigate from Integration Builder to Integration Manager to configure the connections used by your integrations.

## Recommended action

* Start by making sure Integration Manager is installed and up to date in your environment. In Integration Builder, click your user name, select **Settings**, and then in the **Dependencies** tab check the status of Integration Manager. If it's outdated, select **Update dependencies and integrations**.

* If Integration Manager is installed and up to date, ensure the following:

    * If your environment is behind a firewall, check [the network requirements](https://success.outsystems.com/Documentation/11/Setup_and_maintain_your_OutSystems_infrastructure/Setting_Up_OutSystems/OutSystems_network_requirements#integration-builder) and ensure that it allows connections from Integration Builder.

    * Additionally, make sure that requests to the `https://<your.environment.com>/OSIntegrationManager_API/*` endpoint are accessible from Integration Builder.

If the issue persists, please create a case with [OutSystems support](https://success.outsystems.com/Support).
