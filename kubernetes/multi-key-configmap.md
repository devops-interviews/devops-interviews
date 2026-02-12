# Multi Key ConfigMap

> **Company:** Snap | **Difficulty:** Easy

---

#### **Scenario**

An application requires multiple configuration values mounted as files.

#### **Task**

Create a ConfigMap and mount it into a pod so all keys are accessible as files.

| Property | Value |
|----------|-------|
| ConfigMap name | `settings` |
| Key 1 | `MODE=dev` |
| Key 2 | `VERSION=1.0` |
| Pod name | `config-pod` |
| Image | `busybox:latest` |
| Mount path | `/etc/config` |
| Command | `sleep 3600` |
