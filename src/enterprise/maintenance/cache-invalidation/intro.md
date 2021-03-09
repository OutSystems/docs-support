---
summary: Check how cache invalidation works in OutSystems 11.
tags: article-page; version-11
helpids: 30176
---

<pre class="script">
template('OutSystems/OSVersionIndicator');
</pre>

# Cache Invalidation in OutSystems 11

Caching allows applications to temporarily store a given subset of data so that further requests for the same data are done faster, since reading data from cache is a faster operation than reading it again from the database. OutSystems stores cached data of applications in the application server's memory.

Along with cached data itself, OutSystems also stores a reference to the module that produces that data and the tenant where that module exists. To refresh cached data, cache invalidation operations can be done for a module or for a tenant. This process marks cached values in each front-end server as "dirty", and new values are fetched from their original location when needed.

Whenever a request is made, the application server gets any data required for processing the request from memory and, if that data doesn't exist or if it's marked as dirty, it's fetched from its original source.

## How does it work?

The Cache Invalidation Service is the OutSystems component responsible for notifying front-end servers that cached values aren't up-to-date, forcing them to fetch new values when needed.

This service uses a publish/subscribe pattern: applications subscribe to queues that represent modules and tenants where data can come from. The underlying technology used by the Cache Invalidation Service in OutSystems 11 is **RabbitMQ**, a distributed message queue service that implements the publish/subscribe pattern.

The platform must be properly configured so that applications can reach this service. You can install and configure a RabbitMQ instance using OutSystems Configuration Tool. Performing this operation installs RabbitMQ in the same machine that's running the Configuration Tool. Check the [Platform Server 11 Installation Checklist](<https://www.outsystems.com/goto/checklist-11>) for more information on how to install and configure the Cache Invalidation Service.

Every time a cache invalidation occurs for a module or a tenant, all applications watching for changes on these elements are notified, and they flag their local copies as dirty. When the Cache Invalidation Service is down or unavailable (for example, during configuration changes on this service), applications aren't notified of any cache invalidations that might have occurred. This may cause some inconsistent behavior until either these applications can reach the service again or new service configurations are applied. 
To improve the availability of the Cache Invalidation Service you can [configure a RabbitMQ cluster and use a TCP load balancer](<high-availability.md>).
