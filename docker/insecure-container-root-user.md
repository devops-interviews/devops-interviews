# Insecure Container Root User

> **Company:** Accenture | **Difficulty:** Medium

---

#### **Scenario**

A Dockerfile at `/home/interview/Dockerfile` builds a Python web application tagged as `myapp:secure`. The container runs as the root user (UID 0) with extensive Linux capabilities, violating the principle of least privilege.

#### **Task**

Harden the Dockerfile by creating a non-root user `appuser` with UID 10001, switching to that user for application execution, ensuring application files have appropriate permissions, rebuilding the image with the tag `myapp:secure`, and verifying the container `runs` with reduced privileges while maintaining full functionality.

#### **Example**

```
# Before (running as root)

uid=0(root) gid=0(root) groups=0(root)
```

```
# After (running as non-root user)

uid=10001(appuser) gid=10001(appuser) groups=10001(appuser)

Reduced capability set present

Application responds with non-root user confirmation
```

`curl http://localhost:5000/health`
`Response: {"status":"healthy","uid":10001,"user":"appuser"}`

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/insecure-container-root-user)
