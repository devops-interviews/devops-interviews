# Pod Viewer Access

> **Company:** Reddit | **Difficulty:** Easy

---

#### **Scenario**

A monitoring application needs read-only access to pods in the `demo` namespace.

#### **Task**

Set up RBAC so the ServiceAccount can only `get`, `list`, and `watch` Pods in that namespace.

| Property | Value |
|----------|-------|
| Namespace | `demo` |
| ServiceAccount name | `reader-sa` |
| Role name | `pod-reader` |
| RoleBinding name | `pod-reader-binding` |
| Allowed verbs | `get`, `list`, `watch` |
| Resource | `pods` |
