# Log Rotation Size Limit Configuration

> **Company:** DeliveryHero | **Difficulty:** Easy

---

#### **Scenario**

A container image `myapp:logapp` continuously writes logs to stdout. Without log rotation configured, Docker's log files grow unbounded, consuming disk space and potentially filling up the filesystem.

#### **Task**

Run a container from the `myapp:logapp` image with the name `myapp_container`, enable **Docker's built-in log rotation**, configure the maximum size for individual log files to **10MB**, retain maximum  up to `3`  log files during rotation, and verify the container is running successfully.

#### **Example**

```
Multiple rotated log files, each ≤10MB
/var/lib/docker/containers/<id>/<id>-json.log: 8.5MB
/var/lib/docker/containers/<id>/<id>-json.log.1: 10MB
/var/lib/docker/containers/<id>/<id>-json.log.2: 10MB
...
Docker automatically rotates logs at 10MB threshold
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/log-rotation-size-limit-configuration)
