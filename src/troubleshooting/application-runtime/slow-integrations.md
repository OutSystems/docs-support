---
summary: Learn how to deal with slow integrations in your OutSystems apps.
tags: 
locale: en-us
guid: 2BD5C654-4CE7-4752-8407-C9F185D060DB
app_type: traditional web apps, mobile apps, reactive web apps
---

# Dealing with slow integrations triggered by a screen action or by a process

When integrating with external systems, one of the common problems is that such external systems can be very slow. While most of the times there is nothing you can do about that slowness, part of the challenge of developing a great application is hiding that slowness from your end-user (or, at least, manage it in a way that it doesn't cause your own application to become slow).

This article helps you understand the type of problems we are discussing, and suggests an effective way of dealing with it. It includes a sample application which you can use for inspiration when solving the problem.

## The problem

The patterns below can cause extremely slow requests, errors and timeouts:

* Running a slow web-service to show information on a screen.
* Performing a slow query to an external system to reconciliate information with your local data.
* In a BPT flow, call an external system-of-record to close a transaction.

The problems you may find in either of these patterns are:

* The request is very slow, so the screen is left hanging for a long time. Additionally, since OutSystems Platform only allows one concurrent request per end-user session (to avoid corrupting session information), these patterns may lead to the user thinking the server "is down".

* The request [times out](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Timeouts_Under_the_Hood). You may be tempted to overcome the timeout error by increasing the time the request is allowed to run, but then you end-up with problem 1 again.

* In BPT, since you can't to increase the timeout ([it's fixed at 5 minutes](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/BPT_-_Automatic_Activities_Timeout)), you typically get stuck in a timeout, not knowing what to do.


## Dealing with the issue

Solving this type of problem requires that you think **asynchronously**. This means pulling the workload to a separate thread, but leaving your current workload in **idle wait** to avoid starvation (rather than keeping in [busy-waiting](https://en.wikipedia.org/wiki/Busy_waiting), which is always bad).

Multiple solutions exist for idle wait in OutSystems, but one that's relatively simple to implement is:

* Implement a queue mechanism with:

    * Database Entity (storing the parameters to be processed, a boolean on whether it's complete, and a column storing the output).
    * A timer that processes a "queue" of such requests.

* Whenever you need to process something that's slow:

    * Put a new request in the queue.
    * Wake the timer that processes the queue.

* While waiting for the timer to process the queue:

    * If it's something on a screen / end-user UI: send the user to a "waiting" screen that uses polling (every few seconds) to find if the request is already processed (using the boolean column)
    * If it's a BPT: you can use a Wait construct.

* When the queue is finished processing:

    * If it's something on a screen / end-user UI: send the user to the screen when they can proceed (or download, if it's a report).
    * If it's a BPT: the Wait construct ends and skips to the next activity.

For clean-up purposes, don't forget to implement a second timer that runs periodically (for example, every hour) and that deletes all queued requests that have been processed some time ago (such as more than 30 minutes ago).
