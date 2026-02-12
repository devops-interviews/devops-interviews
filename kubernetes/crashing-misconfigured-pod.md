# Crashing Misconfigured Pod

> **Company:** Reddit | **Difficulty:** Medium

---

#### Scenario

You have a Kubernetes cluster where the deployment webapp in namespace prod is stuck in `CrashLoopBackOff`.

The application exposes a health check endpoint at `/healthz` on port `8080`. The container image already includes a config directory with the required files, but the deployment configuration has issues preventing the pod from starting correctly.

Because the config directory already exists and is used by the application, mounting a `ConfigMap` over the entire directory would overwrite it and cause the app to fail. The deployment needs to be fixed so configuration is injected without replacing the existing directory.

#### Task

Fix the pod so it reaches Running state with 1/1 Ready

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/crashing-misconfigured-pod)
