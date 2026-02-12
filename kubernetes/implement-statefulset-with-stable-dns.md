# Implement StatefulSet With Stable DNS

> **Company:** Okta | **Difficulty:** Medium

---

#### **Scenario**

You are deploying a distributed database named `dns-app` in the `dev` namespace. This application requires that each Pod be addressable by a predictable, unchanging hostname (e.g., `dns-app-0.dns-app`) so the nodes can find each other for data replication.

#### **Task**

Create a Headless Service named dns-app in the dev namespace. Create a StatefulSet named dns-app with 3 replicas `image nginx:alpine`. Ensure the StatefulSet uses the dns-app service for network identity. Verify that pods have stable DNS names like dns-app-0.dns-app

Use `kubectl exec -it netshoot -n dev -- nslookup dns-app-0.dns-app` to validate resolution.

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/implement-statefulset-with-stable-dns)
