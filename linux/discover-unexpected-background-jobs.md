# Discover Unexpected Background Jobs

> **Company:** Plus500 | **Difficulty:** Medium

---

#### **Scenario**

You have noticed an unexpected spike in system load. You suspect a batch of recently spawned jobs is responsible and need to isolate processes that started within the last few minutes.

#### **Task**

Identify all processes started within the last **10 minutes** and save their PID, User, Start Date (`lstart`), and Command to `/home/devops/recent_processes.txt`. Once recent processes written to the file Terminate the Suspicious processes (i.e any process that doesn't belong to the root user or systemd).

#### **Example**

The file `/home/devops/recent_processes.txt` should contain the list of recently started processes:

```text
  PID USER     STARTED                     CMD
 8234 deploy   Mon Oct 29 16:37:12 2025    /opt/scripts/deploy.sh
 8235 deploy   Mon Oct 29 16:37:15 2025    bash ./worker_start.sh

```
