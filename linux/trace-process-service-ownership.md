# Trace Process Service Ownership

> **Company:** NVIDIA | **Difficulty:** Hard

---

#### **Scenario**

A process is consuming excessive resources, but its origin is unclear.

#### **Task**

Create a utility script at `/home/devops/trace_service.sh` that accepts a **PID** argument and outputs its managing systemd service name, full status, and the last 20 log entries.

`trace_service.sh Example:`
```sh
#!/bin/bash

PID=$1
echo "PID: $PID"

# Extract service name managing this PID using systemd
# Hint: systemd can resolve a PID back to its unit
SERVICE=""

echo "SERVICE: $SERVICE"

echo "---- STATUS ----"
# Hint: show full systemd status for the identified service with --no-pager flag

echo "---- LOGS ----"
# Hint: show the last 20 log entries for the service from journald with --no-pager flag
```

#### **Example**

Running the script should produce a structured report similar to this:

```text
root@server:~# ./trace_service.sh 4567

Service Identified: nginx.service

--- Status ---
● nginx.service - A high performance web server
   Loaded: loaded (/lib/systemd/system/nginx.service; enabled)
   Active: active (running) since Fri 2025-12-19 14:00:00 UTC; 1h ago
 Main PID: 4567 (nginx)

--- Last 20 Logs ---
Dec 19 14:00:01 server nginx[4567]: Starting web server...
Dec 19 14:00:02 server nginx[4567]: Configuration loaded successfully.
...

```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/trace-process-service-ownership)
