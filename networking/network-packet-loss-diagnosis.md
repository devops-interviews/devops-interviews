# Network Packet Loss Diagnosis

> **Company:** Cloudflare | **Difficulty:** Easy

---

#### **Scenario**

Users are reporting random timeouts. You need to determine whether packet loss occurs on the local network, upstream gateway, or public internet.

#### **Task**

Find your default gateway IP, ping the gateway, DNS server (8.8.8.8), and google.com (5 times each), collect packet loss and average latency from each, and write results to `/tmp/network_diagnostics.txt` showing target name, IP/hostname, packet loss percentage, and average latency.

#### **Example**

**File: /tmp/network_diagnostics.txt**
```
Gateway (192.168.1.1): loss=0% avg=1.2 ms
DNS (8.8.8.8): loss=0% avg=15.8 ms
Internet (google.com): loss=20% avg=83.5 ms
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/network-packet-loss-diagnosis)
