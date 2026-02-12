# Diagnose Nginx CPU Bottleneck

> **Company:** Palantir | **Difficulty:** Easy

---

#### **Scenario**

The web server has become sluggish and users are experiencing timeout errors. Multiple worker processes are running under the `nginx` user, and one of them is consuming excessive CPU resources, causing the entire application to slow down.

#### **Task**

Identify the process running under the `nginx` user that consumes the most CPU or memory, and write its PID to `/home/devops/solution.txt`.

#### **Example**

```
# Before (multiple nginx processes, one consuming excessive resources)

USER       PID   %CPU  %MEM COMMAND
nginx     12345  92.3   4.1 nginx: worker process
nginx     12346  15.4   2.8 nginx: worker process
nginx     12347   1.2   1.0 nginx: worker process
python3   22310  45.7   6.2 python3 app.py
java      19872  37.9  12.4 java -jar app.jar
```

```
# After (PID of highest-consuming nginx process identified)

12345
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/diagnose-nginx-cpu-bottleneck)
