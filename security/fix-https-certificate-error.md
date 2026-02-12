# Fix HTTPS Certificate Error

> **Company:** Github | **Difficulty:** Medium

---

#### **Scenario**

A minimal HTTPS webserver script (`webserver.sh`) listening on port 8443 fails to establish secure connections. The bundled SSL certificate (`old_server.crt`) lacks a **Subject Alternative Name (SAN)** for the local IP `127.0.0.1`, causing hostname verification failures.

#### **Task**

Run the broken server and inspect the certificate to confirm the missing SAN. Generate a new self-signed certificate with SAN set to `IP:127.0.0.1` and save it as `server.crt` and `server.key`. Update `webserver.sh` to use the new certificate files, launch the fixed server, and verify connectivity.

#### **Example**
```text
# Before (Missing SAN)
subject=CN = wrong.example.com
curl: (60) SSL: no alternative certificate subject name matches target host name '1.1.1.1'

# After (SAN Present)
subject=CN = example
X509v3 Subject Alternative Name: IP Address:1.1.1.1
Hello World
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/fix-https-certificate-error)
