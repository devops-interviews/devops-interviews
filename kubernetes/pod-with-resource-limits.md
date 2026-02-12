# Pod With Resource Limits

> **Company:** PWC | **Difficulty:** Easy

---

#### **Scenario**

An application needs guaranteed resources and limits to prevent overconsumption.

#### **Task**

Create a pod with resource requests and limits configured.

| Property | Value |
|----------|-------|
| Pod name | `resource-pod` |
| Image | `nginx:latest` |
| CPU request | `100m` |
| Memory request | `64Mi` |
| CPU limit | `200m` |
| Memory limit | `128Mi` |
