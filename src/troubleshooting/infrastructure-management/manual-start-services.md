---
tags: 
summary: 
locale: en-us
guid: EDE2A61C-EA58-461F-89ED-A434C449A3A9
app_type: traditional web apps, mobile apps, reactive web apps
---

# Manually starting OutSystems services - how-to and caveats

OutSystems Platform uses 5 services:
* Log (OutSystems 10 and previous),
* Deployment Controller (or simply Controller)
* Deployment
* Scheduler
* SMS Connector (OutSystems 10 and previous),

On startup, all 5 services go through several phases. When each phase ends, an information event with the messages below is logged:

| Phase | Event log |
| --- | --- |
| Start | Service started successfully. Waiting for initialization... |
| Initialization | Service initialized successfully. |

## Starting services

The usage of "Stop Services" and "Start Services" by the OutSystems Platform Server are designed for a use-case that's different from the occasional need to do so manually. As such, these shortcuts:

* Stop too many services (more than needed to just "prevent access to the platform").
* May not wait the needed times in a loaded system to always work the same way.

If needed, OutSystems suggests using the relevant primitives from Windows, in a job that waits the needed time and confirms the service has stopped.
For that, [NET STOP](https://technet.microsoft.com/en-us/library/bb490715.aspx) and [NET START](https://technet.microsoft.com/en-us/library/bb490713.aspx) must be used, with each of the following services:

* OutSystems Deployment Controller Service
* OutSystems Deployment Service
* OutSystems Scheduler Service
* OutSystems Log Service
* OutSystems SMS Connector
* msmq (Windows message queuing)

IIS should be started and stopped using appropriate commands: `IISRESET /START` and `IISRESET /STOP`.

### Precedences 

On startup, Log, Controller, and SMS Connector initiate on their own. After they're started, after a limited period in time, they complete initiation.

Deployment and Scheduler, however, need to connect to Controller to initialize successfully. After the Start phase, they try to connect to Controller. If they succeed, they finish starting up
If the connection to the Controller isn't possible, a message similar to the one below is logged in Event Log:

```
Initialization error:

<some error message and stack>

Retrying in 30 seconds

```

Specifically, if the Controller isn't yet started, a message similar to the one attached is shown. The most typical reason for initialization to fail is shown below:

`Initialization error: System.Net.Sockets.SocketException (0x80004005): No connection could be made because the target machine actively refused it 127.0.0.1:12000`

### Retry mechanism

As visible in the message above, services that depend on the Controller have an automatic retry mechanism. This means that, if initialization fails, they wait 30 seconds and try initializing again - and keep doing it until they're able to initialize.
For each failed attempt, an error message is logged in Event Log. When the service finally initializes, the success message is logged.

### Error when starting in the command line

When the service starts via command line, and initialization doesn't succeed, the start yields the error code as you see. However, it's not a permanent failure. This means that the service will try to recover on its own - and keep trying.

Also, the service start doesn't wait until initialization ends. Sometimes (if it's taking longer), "net stop" command may end before service initialized.

It's possible that, during the attempts to initialize, the service doesn't respond adequately to the stop command. This shouldn't be seen as a problem with the service.

### Specific example

To illustrate this with an example from the following log files:

* [Controller log](resources/controller.log)
* [Deployment log](resources/deployment.log)
* [Scheduler log](resources/scheduler.log)
* [Initialization error](resources/initialization-error.txt)

In this case:

* Controller was started at 12:38:31, initialization started at 12:38:55 and ended at 12:39:24
* Deployment was started at 12:38:31, the first attempt to initialize was at 12:38:53. Since init of Controller did not finish yet, it gave an error. Later, the second attempt to initialize at 12:39:31 was successful.
* Scheduler was started at 12:38:32, the first attempt to initialize was at 12:38:53. Since init of Controller did not finish yet, it gave an error. Later, the second attempt to initialize at 12:39:31 was successful.

### Dealing with this behavior

There are two ways to deal with this behavior:

* Trust the service. If everything is well configured, the service will retry initialization until successful.

* Start services in a predetermined order, and wait for a confirmation message. For this, each service should be started, waiting for the initialization confirmation message from Event Log, and then the next one should be started. For the 5 OutSystems services, the following order should be used:

    1. Log
    1. Controller
    1. Deployment
    1. Scheduler
    1. SMS Connector

After each service is started, it's possible to confirm that initialization is correct by consulting Event Log.
