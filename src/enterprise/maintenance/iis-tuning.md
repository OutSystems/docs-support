---
summary: Understanding and fine tuning ASP.NET process model settings on a Microsoft Internet Information Services (IIS) Web Server for use with OutSystems. 
---

# Tuning Microsoft Internet Information Services (IIS) Web server for use with OutSystems

ASP.Net gives system administrators a way for them to manage aspects of the ASP.NET worker process like the size of the CLR thread pool to service requests, the number of instances created at a time, to name a few. In the configuration file the element that lets us configure these behaviours is the processModel element, present in the machine.config.
By default all configurations should start with the parametrization

`<processModel autoConfig="true" />`

This is set by the platform when running the configuration tool. Setting the autoConfig to true will make IIS worker process manage the following attributes:
* maxWorkerThreads;
* maxIoThreads;
* minFreeThreads;
* minLocalRequestFreeThreads;
* maxConnection.

It will be irrelevant the values that we assign to the above attributes if you have the autoConfig set to true. IIS worker process will fully control their values. The values of the attributes above are set based on the following rules:
* maxWorkerThreads = 100 (this value is per CPU);
* maxIoThreads = 100 (this value is per CPU);
* minFreeThreads = 88 * <Number of CPUs>;
* minLocalRequestFreeThreads = 76 * <Number of CPUs>;
* maxConnection = Int32.MaxValue.

Even though the autoconfig set to true is the recommended setting this does not work well with bursts of requests. IIS worker process analyses its state in a period of time too slow for it to react to handle a burst of requests. This configuration works better in steady increases in the workload.

Despite the above attributes being governed internally by ASP.Net, we can tweak the values of the attributes minIoThreads and minWorkerThreads. Both these attributes only make sense having values between 89 and maxIoThreads, and maxWorkerThreads, respectively, that is 100 by default. The values are 1) 89 because it doesn’t make sense to have fewer threads configured than the magic 88 in the minFreeThreads and; 2) the 100 is self explanatory because it is the max value for the number of Io and Worker threads.

<div class="info" markdown="1">
Since version PS11.10.0 the values of minIoThreads and minWorkerThreads are automatically set by configuration too to 100. However you may need to tune them further. If the values are already set by the system administrator configuration tool will honor them.
</div>

The minWorkerThreads and minIoThreads define the minimal number of threads the IIS worker process will spin up in a short amount of time. After this threshold is reached, spinning up a new thread takes longer. This is the point referred above about the adaptive nature of the autoConfig attribute. Under unusual circumstances, like a burst of requests, the request count can go up quickly making IIS struggle to spin new threads leading to queued requests. This point is important because OutSystems’ Mobile and Reactive applications are “bursty” in nature. Accessing a single page can generate multiple requests in burst to the server. If you have a Front End dedicated to one of these types of applications, tuning minWorkerThreads and minIoThreads values is of particular importance.

<div class="warning" markdown="1">
Any change to the ProcessModel element only becomes effective once you restart the IIS worker service.
</div>

Now lets see the impact of setting the values of minIoThreads and minWorkerThreads in the Front End. For clarity, let's assume we have a Front End with 4 CPUs and that we set minIoThreads and minWorkerThreads to 100, what we are saying is that the IIS worker process will be fast to spin up 100 threads per CPU and have them ready to handle requests. This implies that if we take the magic thread number of 88 into account, we have 12 “dedicated” threads to handle requests per CPU. Meaning that with this configuration, your Front End would have 48 threads capable of handling requests in parallel available at the start of the worker process.

A note, we suggest that minIoThreads and minWorkerThreads attributes share the same value.

Increasing the number of threads readily available to handle requests have impact in the overall system. More requests handled per second means that the resources that support those requests are also under increased load. Things like Database, external SOAP, REST services, to name a few. For this reason there are some considerations to have when tweaking the values of minIoThreads and minWorkerThreads attributes:
* Remember that by default OutSystems sets the Max Pool Size to 100. If your configuration is capable of more than 100 request in parallel you can exhaust all the connections in the pool;
* Remember that every service consumed or connected by the application will have it’s load increased;
* For O10 only, remember that we might need to increase the message queue size.