# Managing High I/O Processes

> **Company:** Revolut | **Difficulty:** Easy

---

#### **Scenario**
Users are complaining about slow file access. System metrics show high disk utilization.

#### **Task**
Reduce `I/O` activity of top offender using I/O priorities to `idle`. Keep critical jobs (databases, message queues, applications) at high priority.


#### **Example**

```
 # Before (high I/O contention)

 Total DISK READ:      45.67 M/s | Total DISK WRITE:     123.45 M/s

   TID  PRIO  USER      DISK READ  DISK WRITE  COMMAND
  5678  be/4  backup     2.34 M/s   98.76 M/s  rsync /data /backup
  3421  be/4  postgres  15.23 M/s   12.45 M/s  postgres: vacuum
  8234  be/4  appuser    8.45 M/s    3.21 M/s  /usr/bin/log-processor

 # After (non-critical jobs throttled)

 Total DISK READ:      18.34 M/s | Total DISK WRITE:      35.21 M/s

   TID  PRIO  USER      DISK READ  DISK WRITE  COMMAND
  5678  idle  backup     0.50 M/s    2.10 M/s  rsync /data /backup
  3421  be/4  postgres  15.23 M/s   12.45 M/s  postgres: vacuum
  8234  idle  appuser    1.20 M/s    0.80 M/s  /usr/bin/log-processor

```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/managing-high-io-processes)
