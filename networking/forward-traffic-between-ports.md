# Forward Traffic Between Ports

> **Company:** Meta | **Difficulty:** Medium

---

#### **Scenario**

A service on your server is running on **port 8080**, but you now need it to also be reachable on **port 8081**. The application cannot be restarted and its configuration cannot be changed.

#### **Task**

Verify the service is listening on `127.0.0.1:8080`. Configure `iptables` to forward all TCP traffic from **port 8081** to **port 8080**, ensuring this works for both external requests and local connections (localhost). Verify the forwarding works, then save the rules to persist after a reboot using `iptables-save`

#### **Example**

```
tcp        0      0 127.0.0.1:8080          0.0.0.0:*               LISTEN      1234/java

PREROUTING (policy ACCEPT)
REDIRECT   tcp  --  0.0.0.0/0   0.0.0.0/0   tcp dpt:8081 redir ports 8080

OUTPUT (policy ACCEPT)
REDIRECT   tcp  --  0.0.0.0/0   127.0.0.1   tcp dpt:8081 redir ports 8080
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/forward-traffic-between-ports)
