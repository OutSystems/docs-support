---
summary:
tags: 
locale: en-us
guid: 64497876-fac0-409b-b7d9-9456e44086bf
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# Java server logs

### JBoss logs

To obtain the JBoss logs for a specific environment, follow these steps:

1. Connect to the server.

1. Find the log files at:
     * JBoss 5: /opt/jboss-5.1.0.GA/server/outsystems/log
     * JBoss 7: /opt/jboss-as-7.1.1.Final/standalone/log

If you are getting these logs by request of OutSystems Support, zip all the files and **attach the zip file to your support case**.

### WildFly logs

To obtain the WildFly logs for a specific environment, follow these steps:

1. Connect to the server.

1. Find the log files at:
     * WildFly 8.2: /opt/wildfly-8.2.0.Final/`<wbr/>`standalone/log

If you are getting these logs by request of OutSystems Support, zip all the files and **attach the zip file to your support case**.

### WebLogic logs

To obtain the WebLogic logs for a specific environment, follow these steps:

1. Connect to the server.

1. Find the log files at:
     * Admin Server logs: /opt/Oracle/Middleware/user_projects/domains/outsystems_domain/servers/AdminServer/logs
     * Managed Server logs: /opt/Oracle/Middleware/user_projects/domains/outsystems_domain/servers/`<ManagedServerName>`/logs


