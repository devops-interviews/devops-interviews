# CronJob Schedule Misconfiguration

> **Company:** RedHat | **Difficulty:** Medium

---

#### **Scenario**

A CronJob named `cleanup` in the `ops` namespace is failing to trigger as expected. It has an incorrect schedule, relies on the default timezone (which may not match the server), and retains too many completed jobs, cluttering the history.

#### **Task**

Fix the cleanup `CronJob` so that validation confirms it triggers exactly once per minute. Update the schedule to `* * * * *`, set the timezone to `Etc/UTC`, and ensure only the most recent successful run is retained.

#### **Example**

**Current Status (Failing):**
```
NAME      SCHEDULE    SUSPEND   ACTIVE   LAST SCHEDULE   AGE
cleanup   0 0 1 1 *   False     0        <none>          5m
```

**Target Status (Success):**
```
NAME      SCHEDULE    SUSPEND   ACTIVE   LAST SCHEDULE   AGE
cleanup   * * * * *   False     0        10s             7m
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/cronjob-schedule-misconfiguration)
