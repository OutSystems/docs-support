# No-downtime deployments with Azure

## Upgrading application versions on Azure ACS

The ACS (Azure Container Service) Engine uses Kubernetes in its core, and application deployments are done using Kubernetes deployments.

You can apply several deployment strategies when using Kubernetes, being the most common one the **rolling update** strategy.

With this update strategy the update takes place with no downtime by incrementally updating Pods instances with new ones.
