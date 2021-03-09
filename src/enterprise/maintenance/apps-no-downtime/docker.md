# No-downtime deployments with Docker

# Upgrading application versions in Docker Swarm

Docker Swarm performs **rolling updates by default** when you run the following command:

```
docker service update
```

Therefore, you will get a no-downtime application version upgrade with no need for further actions.

This command will instantiate the new container replicas and then stop the previous ones. Both the old and the new application versions will coexist during a small time frame.
