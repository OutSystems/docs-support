---
summary: Understand, troubleshoot and resolve an error that occurs when debugging a Reactive Web application in Service Studio
tags: 
---

# Error loading the application for debugging - debugging session will not continue

## Symptoms

When you start debugging a Reactive Web application in Service Studio, a Chrome window opens with the following error message: 

`There was an error loading the application for debugging. The debugging session will not continue.`

![Error message](images/error-debugging-ss.png)

## Cause

This error occurs when there is a delay connecting Service Studio and Chrome. This delay usually occurs when the user has a proxy server configured on their machine.

## Solution

You can solve this problem in one of the following ways:

* Don't close the Chrome window and click the **Start Debugging** button again. The Chrome window is reused and you can start debugging on the **Debug** tab in **Service Studio**.

* Go to [chrome://settings/?search=proxy](chrome://settings/?search=proxy) and click **Open your computer's proxy settings** then disable Automatically detect settings. 

    ![Error solution](images/error-debugging-solution.png)

    What does this setting do? Proxy auto-detect works via DNS queries. It finds out where to fetch JavaScript files that run on every hit that the browser loads to determine the correct way to retrieve what it needs. By disabling it, it takes less time to create the connection between Service Studio and Chrome, allowing the debug session to start successfully.
