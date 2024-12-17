---
summary: Explore the limitations and data extraction methods of OutSystems 11 (O11) personal environments, hosted on a multi-tenant infrastructure.
locale: en-us
guid: 5b26b215-56f9-460e-9794-f4b7fcb15a16
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
tags: personal environment, multi-tenant architecture, data storage, api, data export
audience:
  - mobile developers
  - frontend developers
  - full stack developers
outsystems-tools:
  - none
coverage-type:
  - understand
---

# Personal environment hosting infrastructure under the hood

A Personal Environment is an OutSystems platform running on a multi-tenant, shared infrastructure.

Regardless of the (ever changing) underlying hardware, each personal environment has the following limitations:

* Multi-tenant shared infrastructure where the available resources (CPU, memory, IO) are limited by usage thresholds per environment

* Maximum of 2 GB for database storage of system and application data

* No caching is available

* No support for team collaboration

* Application versions are automatically deleted after two weeks

## Extracting your data

In a personal environment, you can't directly access the front-end or database servers. This ensures you have the best possible experience.

If you want to extract your data, you can:

* [Expose a REST API ](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/REST/Expose_REST_APIs/Expose_a_REST_API) that makes your data available

* Implement functionality that allows [downloading an Excel file](https://success.outsystems.com/Documentation/How-to_Guides/Data/How_to_Export_Entity_Data_to_Excel) with the data

## More Information

To learn more about personal environments, see [What is a personal environment?](whats-a-personal.md).

