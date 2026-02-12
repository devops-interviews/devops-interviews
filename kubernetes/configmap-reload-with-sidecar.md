# ConfigMap Reload With Sidecar

> **Company:** Yelp | **Difficulty:** Medium

---

#### **Scenario**

Your application needs to react to configuration changes without requiring a pod restart.

#### **Task**

Create a ConfigMap and a pod with a sidecar that watches for configuration file changes. Mount the ConfigMap to both containers.

| Property | Value |
|----------|-------|
| Namespace | `default` |
| ConfigMap | `app-config` |
| ConfigMap key | `settings.conf` |
| ConfigMap value | `debug=false` |
| Pod | `app-pod` |
| Main container | `app` |
| Main image | `nginx:1.24` |
| Sidecar container | `config-watcher` |
| Sidecar image | `busybox` |
| Mount path | `/etc/config` |

Sidecar container snippet is at `/home/interview/watcher.yaml`.

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/configmap-reload-with-sidecar)
