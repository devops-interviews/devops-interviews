# DNS Based Service Discovery

> **Company:** Netflix | **Difficulty:** Medium

---

#### **Scenario**

In namespace `disco`, the application `discovery-app` relies on DNS-based discovery of peer pods. The service `discovery-svc` is supposed to return all backend pod IPs, but currently:

```bash
kubectl exec deploy/testpod -n disco -- nslookup discovery-svc.disco.svc.cluster.local
```

returns only one IP instead of individual pod IPs. The application cannot discover its peers and fails to form a cluster.

#### **Task**

Fix the service configuration so that DNS resolution of `discovery-svc` returns one IP per pod, allowing the application to discover all running instances.

| Property | Value |
|----------|-------|
| Namespace | `disco` |
| Deployment | `discovery-app` (3 replicas) |
| Service | `discovery-svc` |
| Pod label | `app=discovery` |
