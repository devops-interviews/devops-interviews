# Traffic Splitting With Native Kubernetes

> **Company:** Palantir | **Difficulty:** Medium

---

#### **Scenario**

Your team has a stable deployment `app-v1` running in namespace `canary`. They want to test a new version (v2) with approximately 1/3 of traffic going to v2 and 2/3 remaining on v1.

#### **Task**

Implement canary traffic splitting between both versions using only native Kubernetes resources.

| Property | Value |
|----------|-------|
| Namespace | `canary` |
| Existing deployment | `app-v1` |
| Canary deployment | `app-v2` |
| Canary image | `nginx:1.25` |
| Service name | `my-app-svc` |
| Service port | `80` |

A reference deployment file is available at `/home/interview/deployment.yaml`.

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/traffic-splitting-with-native-kubernetes)
