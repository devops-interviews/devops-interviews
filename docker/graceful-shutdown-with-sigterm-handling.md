# Graceful Shutdown with SIGTERM Handling

> **Company:** Robinhood | **Difficulty:** Medium

---

#### Scenario:

You have a container image `myapp:grace` built from `/home/interview/Dockerfile` that runs an application requiring cleanup on shutdown. When you run `docker stop`, the container is killed after the 10-second timeout instead of shutting down gracefully because the application doesn't properly handle the SIGTERM signal.

#### Task:

Fix the application script and Dockerfile to properly handle SIGTERM signals, implement cleanup logic, and ensure the container exits gracefully within 20 seconds when `docker stop` is executed.

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/graceful-shutdown-with-sigterm-handling)
