# Temporary Route Configuration

> **Company:** Spotify | **Difficulty:** Easy

---

#### **Scenario**

You need to reach a remote subnet that isn't covered by the default route, but you don't want to make any permanent configuration changes.

#### **Task**

Check the current routing table to confirm the `10.20.0.0/16` subnet is not present, add a temporary static route for the `10.20.0.0/16` subnet via gateway `192.168.1.1` using interface `veth0`.

#### **Example**

```
# Before (no route to remote subnet)

10.20.0.0/16 subnet not in routing table
Cannot reach remote network
Need temporary access without permanent changes
```

```
# After (temporary route added)

10.20.0.0/16 via 192.168.1.1 dev veth0

Route active and verified
Remote subnet accessible
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/temporary-route-configuration)
