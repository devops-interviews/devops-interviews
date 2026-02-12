# Validating Network Routes

> **Company:** Google | **Difficulty:** Medium

---

#### **Scenario**

Your server uses multiple network interfaces and may have incorrect routing for a specific subnet. You need to verify and fix it to ensure proper traffic flow.

#### **Task**

Display the current routing table to identify existing routes, check if a route for the `10.10.0.0/16` subnet exists and which interface and gateway it uses. If the route goes through `eth0`, delete the existing route and add a new route for `10.10.0.0/16` via gateway `192.168.100.1` using interface `eth1`.

#### **Example**

```
# Before (incorrect route through eth0)

10.10.0.0/16 routed via eth0
Gateway: 192.168.50.1
Traffic experiencing packet loss
```

```
# After (corrected route through eth1)

10.10.0.0/16 routed via eth1
Gateway: 192.168.100.1
Route verified and active
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/validating-network-routes)
