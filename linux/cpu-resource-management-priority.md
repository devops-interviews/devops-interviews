# CPU Resource Management Priority

> **Company:** RedHat | **Difficulty:** Easy

---

#### **Scenario**

During peak traffic hours, a background `data-processing` job that is started by user `devops` is consuming too much CPU and slowing down user-facing services. Stopping it isn't an option because it would interrupt ongoing workflows, but you need to limit its CPU usage temporarily.

#### **Task**

Reduce the process's priority to `10` while keeping it running.

#### **Example**

```
# Before (high priority process)

USER       PID %CPU %MEM    VSZ     RSS   TTY      STAT START   TIME COMMAND
devops    5432 85.3 12.4 2048576 256840   ?        RN   14:35   8:23 /usr/bin/data-processor --batch
```

```
# After (priority adjusted)

USER       PID %CPU %MEM    VSZ     RSS   TTY      STAT START   TIME COMMAND
devops    5432 45.2 12.4 2048576 256840   ?        RN   14:35   8:45 /usr/bin/data-processor --batch
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/cpu-resource-management-priority)
