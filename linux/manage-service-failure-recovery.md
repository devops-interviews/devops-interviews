# Manage Service Failure Recovery

> **Company:** Apple | **Difficulty:** Hard

---

#### **Scenario**

You have a shell script at `/usr/local/bin/check_app.sh` that runs periodically and exits with a non-zero code. The script is currently failing due to a simulated error condition.

#### **Task**

Create a `systemd service` named `check_app.service` that automatically restarts the script when it fails, but stops retrying after `3 restart` attempts within `60 seconds`. Configure the service to start on boot with a `5-second delay` between restart attempts, then start the service and verify it hits the restart limit.

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/manage-service-failure-recovery)
