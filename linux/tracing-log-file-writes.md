# Tracing Log File Writes

> **Company:** Bloomberg | **Difficulty:** Easy

---

#### **Scenario**

The `/var/log/messages` file has been growing unusually fast, filling up disk space within hours.

#### **Task**

Identify the process that is writing heavily to `/var/log/messages` by monitoring system activity in real time. Save the process details using `ps` and last `50` lines of logs at `/home/devops/excessive_log_process.txt`

#### **Example**

```
# Before (log file growing rapidly)

/var/log/messages: 15 GB and increasing
Disk usage: 92% and climbing
```

```
# After (responsible process identified)

Process identified: rsyslogd (PID 1234)
Confirmed active writes to /var/log/messages
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/tracing-log-file-writes)
