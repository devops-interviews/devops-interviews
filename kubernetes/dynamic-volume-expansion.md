# Dynamic Volume Expansion

> **Company:** EPAM | **Difficulty:** Easy

---

#### **Scenario**

An application requires persistent storage that can be resized without downtime.

#### **Task**

Create a StorageClass, PVC, and Pod. Once the pod is running, expand the PVC to the expanded size without restarting the pod.

| Property | Value |
|----------|-------|
| Namespace | `storage` |
| StorageClass | `expandable-sc` |
| PVC name | `data-pvc` |
| Initial size | `1Gi` |
| Expanded size | `5Gi` |
| Pod name | `app-pod` |
| Image | `nginx` |
| Mount path | `/data` |

Template files are available at `/home/interview/`.

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/dynamic-volume-expansion)
