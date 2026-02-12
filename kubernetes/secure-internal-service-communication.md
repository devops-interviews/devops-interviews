# Secure Internal Service Communication

> **Company:** Dropbox | **Difficulty:** Medium

---

#### Scenario

An application requires TLS certificates for internal service communication.

#### Task

Setup cert-manager to issue a valid TLS certificate using a SelfSigned ClusterIssuer to bootstrap a CA Issuer.

| Property | Value |
|----------|-------|
| Namespace | `preparesh` |
| SelfSigned ClusterIssuer | `selfsigned-issuer` |
| CA Certificate name | `ca-cert` |
| CA secret name | `ca-secret` |
| CA Issuer name | `ca-issuer` |
| CA Issuer CN | `preparesh-ca` |
| Certificate name | `web-cert` |
| Certificate secret | `web-cert-tls` |
| DNS names | `web.preparesh.svc`, `web.preparesh.svc.cluster.local` |

Template files available at `/home/interview/`.

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/secure-internal-service-communication)
