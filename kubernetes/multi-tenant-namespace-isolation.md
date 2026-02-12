# Multi Tenant Namespace Isolation

> **Company:** Palantir | **Difficulty:** Medium

---

#### **Scenario**

Two teams share a cluster and require strict isolation with specific exceptions for inter-team communication.

#### **Task**

Configure network isolation and resource constraints for both teams:

1. Create default deny NetworkPolicies for both namespaces (deny all ingress and egress traffic)
2. Create a NetworkPolicy allowing `team-a` pods to access `team-b` pods labeled `app=api` on port `8080` only
3. Create LimitRanges in both namespaces to enforce maximum resource limits per container

| Property | Value |
|----------|-------|
| **Namespace 1** | `team-a` |
| **Namespace 2** | `team-b` |
| **Allowed communication** | `team-a` → `team-b` pods with label `app=api` on port `8080` only |
| **Default traffic** | Deny all other cross-namespace traffic |
| **Max CPU per container** | `1` |
| **Max Memory per container** | `512Mi` |

_Note: Test pods are already deployed - `client` in `team-a`, and `api` + `web` in `team-b`._
