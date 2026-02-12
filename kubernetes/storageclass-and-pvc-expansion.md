# StorageClass and PVC Expansion

> **Company:** Datadog | **Difficulty:** Medium

---

#### Scenario

The cluster has no StorageClass configured for dynamic volume expansion.

#### Task

Create a **StorageClass** with volume expansion enabled, create a **PVC** and **Pod** using it, then expand the **PVC** from `1Gi` to `2Gi`.

| Property | Value |
|----------|-------|
| Namespace | `storage` |
| StorageClass name | `fast-sc` |
| PVC name | `expand-pvc` |
| Initial PVC size | `1Gi` |
| Expanded PVC size | `2Gi` |
| Pod name | `storage-pod` |
| Pod image | `nginx` |
| Mount path | `/data` |

Resource templates are available at `/home/interview/`.

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/storageclass-and-pvc-expansion)
