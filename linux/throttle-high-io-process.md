# Throttle High I/O Process

> **Company:** Ebay | **Difficulty:** Easy

---

#### **Scenario**

A server is experiencing latency spikes and intermittent timeouts. CPU and memory appear normal, suggesting a disk I/O bottleneck from a runaway process.

#### **Task**

Identify the process causing high disk I/O using real-time monitoring, then apply I/O throttling to reduce its disk priority to idle class without terminating it.

#### **Example**

```
# Before (high I/O process)

Total DISK READ:       125.43 M/s | Total DISK WRITE:        89.32 M/s
  TID  PRIO  USER     DISK READ  DISK WRITE  SWAPIN     IO>    COMMAND
 5432 be/4 postgres   98.45 M/s   67.23 M/s  0.00 %  95.32 % postgres: autovacuum worker
```

```
# After (I/O throttled)

Total DISK READ:        12.34 M/s | Total DISK WRITE:         8.92 M/s
  TID  PRIO  USER     DISK READ  DISK WRITE  SWAPIN     IO>    COMMAND
 5432 idle postgres    9.12 M/s    6.45 M/s  0.00 %  12.34 % postgres: autovacuum worker
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/throttle-high-io-process)
