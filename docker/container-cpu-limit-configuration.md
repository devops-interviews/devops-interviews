# Container CPU Limit Configuration

> **Company:** IBM | **Difficulty:** Easy

---

#### Scenario:

You have a container named `cpu_test` running from the image `myapp:cpu` that performs CPU-intensive computations. When monitoring with **docker stats**, the container regularly spikes to **150-200% CPU usage**, consuming multiple CPU cores and impacting other services on the host.

#### Task:

Update the container configuration to limit CPU usage so that `docker stats` shows the `cpu_test` container consistently using **less than 60% CPU** during validation; You need to assign `500m` CPU for that.

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/container-cpu-limit-configuration)
