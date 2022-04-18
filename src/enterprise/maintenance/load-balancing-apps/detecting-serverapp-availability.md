---
summary:
en_title: 02 Detecting OutSystems server//app availability
locale: en-us
guid: 4f019a61-013f-4cac-be80-05b0abff742b
app_type: traditional web apps, mobile apps, reactive web apps
---

# Detecting OutSystems server/app availability

To detect that a front-end is up and running in your on-premises/private cloud installation, you can monitor the TCP port that is serving the applications or web services, the most common ones are TCP port 80 (HTTP) and TCP port 443 (HTTPS).

With an L7 load balancer you get a more complete form of monitoring, going beyond the simple check whether the server is up or down.

![ ](images/detecting-serverapp-availability_0.png)

A best practice is to create a specific webscreen in your application that performs basic business validations. This ensures the system is up and outputs a specific string when everything is OK. In this webscreen you should test critical integrations (e.g. web-services, external databases

By implementing this in a webscreen, by default, you perform a test that OutSystems Platform is working, for the whole stack, in that Front-end (e.g.app server, database).

If the load balancer supports it, you can use this webscreen to create a web check and test it by looking for a specific string the page writes if all tests pass.

## More information

To learn more about how to load balance your OutSystems Platform check the [Load Balancing OutSystems Applications](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Load_Balancing_OutSystems_Applications) guide.
