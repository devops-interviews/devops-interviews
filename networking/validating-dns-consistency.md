# Validating DNS Consistency

> **Company:** SAP | **Difficulty:** Easy

---

#### **Scenario**

Your monitoring alerts indicate that DNS resolution might be inconsistent across servers, and you need to confirm both IPv4 and IPv6 records for a given domain.

#### **Task**

Add IPv4 and IPv6 address entries for the domain `example.local` to `/etc/hosts` using the format `<ip_address> <hostname>` with each record on a separate line.

#### **Example**
```
198.51.100.42 example.local
2001:db8:85a3::8a2e:370:7334 example.local
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/validating-dns-consistency)
