# Network Socket Usage Analysis

> **Company:** SAP | **Difficulty:** Easy

---

#### **Scenario**

Network latency issues were reported due to opening too many TCP connections.

#### **Task**
Inspect active sockets along with the processes that own them to identify which application is responsible for the excessive connection count. Save all currently active TCP/UDP connections (ESTABLISHED, LISTEN, TIME_WAIT, etc.) output to `/tmp/active_tcp.txt`

#### **Example**
```
Proto Recv-Q Send-Q Local Address           Foreign Address         State       PID/Program name
tcp        0      0 192.168.1.50:22         192.168.1.100:54321     ESTABLISHED 1234/sshd
tcp        0      0 192.168.1.50:3306       192.168.1.75:41234      ESTABLISHED 5678/mysqld
tcp        0      0 0.0.0.0:80              0.0.0.0:*               LISTEN      9012/nginx
tcp        0      0 127.0.0.1:6379          127.0.0.1:45678         ESTABLISHED 3456/redis-server
tcp        0      0 192.168.1.50:443        203.0.113.45:12345      ESTABLISHED 9012/nginx

```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/network-socket-usage-analysis)
