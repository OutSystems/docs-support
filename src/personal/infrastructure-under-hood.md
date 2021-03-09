---
summary: A personal environment is an OutSystems platform running on a shared infrastructure, with limited computing resources, max 2GB data, and no team collaboration.
---

# Personal environment hosting infrastructure under the hood

A Personal Environment is an OutSystems platform running on a multi-tenant, shared infrastructure.

Regardless of the (ever changing) underlying hardware, each personal environment has the following limitations:

* Multi-tenant shared infrastructure where the available resources (CPU, memory, IO) are limited by usage thresholds per environment;

* Maximum of 2 GB for database storage of system and application data;

* No support for team collaboration;

* Application versions are automatically deleted after two weeks.

## Extracting your data

In a personal environment, you can't directly access the front-end or database servers. This is made to ensure you have the best possible experience.

If you want to extract your data, you can:

* [Expose a REST API ](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/REST/Expose_REST_APIs/Expose_a_REST_API)that makes your data available;

* Implement functionality that allows [downloading an Excel file](https://success.outsystems.com/Documentation/How-to_Guides/Data/How_to_Export_Entity_Data_to_Excel) with the data.

## More Information

To learn more about personal environments, check [What is a personal environment?](whats-a-personal.md)

