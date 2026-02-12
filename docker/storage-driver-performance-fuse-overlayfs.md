# Storage Driver Performance Fuse Overlayfs

> **Company:** Github | **Difficulty:** Medium

---

#### Scenario:

You have a container image `myapp:fs` built from `/home/interview/Dockerfile` that performs intensive filesystem write operations. Docker is currently using the **overlayfs storage driver**  and write performance is a bottleneck.

#### Task:

Configure Docker deamon `/etc/docker/daemon.json` to use appropriate configuration for write heavy setup. Restart the Docker daemon, and rebuild the `myapp:fs` image for validation testing.

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/storage-driver-performance-fuse-overlayfs)
