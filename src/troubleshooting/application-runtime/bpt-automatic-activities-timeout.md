---
summary:
locale: en-us
guid: 4728654c-0e38-49cd-9e9a-789e1fe5c052
app_type: traditional web apps, mobile apps, reactive web apps
---

# BPT - Automatic Activities Timeout

## Overview

When building processes using our Business Process Technology (BPT) you may build automatic activities which hit a pre-defined timeout. The predefined timeout for BPT Automatic Activities is 5 minutes. What should you do if your process is hitting this limit?

### Context

BPT processes are used for a variety  of reasons. They are mainly used to model real-life processes and automate some of the parts of those processes (this is where automatic activities are used). But they can also be used as a way to implement some sort of asynchronous behavior.

BPT was designed specifically for the former, but can be (to an extent) used for the latter purpose.

## Problems

Each BPT instance does not spawn a new thread which is running to process that specific instance. Instead a pool of threads is used which advances each process instance in turn. If you have a long running batch process running on an automatic activity, this will use up one of those threads. If you have a lot of these, all threads (or a significant amount of threads) will be used up by these activities and this may prevent other process instances from progressing.

In an attempt to avoid these scenarios, OutSystems has implemented a timeout of 5 minutes to all automatic activities. Given  that the BPT architecture is not prepared to process a lot of long-running automatic activities, this timeout is for any and all automatic activities and cannot be "personalized", like timeouts for web reference calls and timers.

This means that if you have an automatic activity that is hitting the 5 minute threshold, maybe it's time to review it in order to perform these (usually) batch operations in a more scalable manner.

## Resolution

The solution for this is usually a restructure of your BPT process to use the established mechanisms for batch processing instead of BPT. In short, you will need to use timers for the job.

The idea is that your automatic activity which takes more than 5 minutes will now be processed in a Timer. The activity in the BPT process simply prepares the workload for the timer and (optionally) launches the timer. After this the process Waits for the timer to do what it needs to do.

The timer processes the data and at the end signals the waiting BPT process to proceed. This can be done by directly closing the Wait activity, or by updating or creating an entity.

