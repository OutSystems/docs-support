---
summary: Identify and resolve the publication error "The process cannot access the file because it is being used by another process".
Tags: 
locale: en-us
guid: 1305808c-05bc-4f19-939b-09877f5681c1
app_type: traditional web apps, mobile apps, reactive web apps
---

# Publish error - the process cannot access the file

## Symptom

When publishing either on Service Studio, Service Center or even when deploying to another environment on LifeTime, an error occurs that states:

`The process cannot access the file because it is being used by another process`

This error occurs in the compilation stage and the publication process fails.

## Causes

This error is caused by concurrency when two or more different processes try to access and lock the same file.
A quick action you can take is to wait a few minutes and then try to publish again.

So that you can troubleshoot the cause and prevent this from happening again, we'll list the most common causes, in order.

The presented causes and their respective solutions apply to self-managed OutSystems environments. This is not expected to occur while publishing on an OutSystems cloud environment. However, if that's ever the case, [contact OutSystems Support](https://www.outsystems.com/goto/submit-support-case).

### Antivirus software

This is the most common cause for this error. 

#### Problem

Antivirus software may perform regular scans on the Platform Server's files and while doing so, locks the files. Antivirus checks can be triggered when the Platform Server is generating new source code during publication. If the Platform Server accesses a file that's locked by an antivirus, this error occurs.

#### Solution

OutSystems recommends to [exclude some folders from antivirus scanning](https://success.outsystems.com/Documentation/Best_Practices/Performance/Performance_Best_Practices_-_Infrastructure#Exclude_some_folders_from_antivirus_scanning). Make sure that those folders are on the exclusions list. If they aren't, add them and retry the publication.


### Other processes

Various other processes from third party software may also lock OutSystem files while the Platform Server is trying to access them. 

You can identify the specific process with tools like [Process Explorer](https://docs.microsoft.com/en-gb/sysinternals/downloads/process-explorer) or [Process Monitor](https://docs.microsoft.com/en-gb/sysinternals/downloads/procmon). 

Identifying the process and the program running it allows you to act on it, either by killing the process or reconsidering the use of those programs. While the way to tackle it highly varies with the program at hand, these tools provide the information necessary to make a decision.
