# Pod With Readiness Probe

> **Company:** Zscaler | **Difficulty:** Easy

---

#### **Scenario**

You need to deploy a web application that only receives traffic when it's ready to serve requests.

#### **Task**

Create a pod with an HTTP readiness probe that checks if the service is responding on port `80` at path `/`.

| Property | Value |
|----------|-------|
| Pod name | `web-ready` |
| Image | `nginx:latest` |
| Probe type | HTTP GET |
| Probe port | `80` |
| Probe path | `/` |
