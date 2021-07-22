---
summary: Typical reasons for the debugger to hang or stop working in the middle of a debugging session. Check the causes and the solutions.
---

# Debugger not working

## Symptoms

* In a debug session, the debugger never reaches a breakpoint.
* In the middle of a debug session, the debugger just hangs.
* The debugger stops working.

## Cause

During a debug session, Service Studio contacts the environment where the app is deployed. During the session it communicates back and forth several times with the environment. To keep communications fast,  Service Studio keeps an open connection to the environment.

Depending on your anti-virus, firewall, or other network elements you might have in place, it's possible that these elements abruptly close the connection between  Service Studio and the environment.

And that's when the debugger hangs.

## Solution

Configure Service Studio so that it establishes a new connection for each request made to the environment.

In **Edit** menu, under **Preferences**, check the **Use One Connection per Request in Debugger** option.

By activating this option, it's possible that the debugger feels slower since it's establishing new connections on each request.


# The server stops the debug session

## Symptoms

* In a debug session, Service Studio informs that "The server has stopped the debug session".
* When checking the Service Studio error report, it shows the following error message: "There was an error while contacting the server: HTTP Forbidden"

## Cause

This usually occurs on on-premises environments, when there are additional network elements, like internal/external load balancers or reverse proxies, that you need to inform the OutSystems Platform that they are trusted.

## Solution

In order for you to configure a trusted proxy in your on-premises environment, please proceed as follows:

1. Access Service Center in your environment;
2. Go to Administration > Security > Network Security;
3. Add the IP addresses or IP ranges of all network elements in the Trusted proxy addresses field.

## More information

There might be other problems affecting your debug session. Check [other reasons](http://www.outsystems.com/forums/discussion/10962/tip-service-studio-is-not-always-stopping-in-my-breakpoints/) for the debugger to misbehave.
