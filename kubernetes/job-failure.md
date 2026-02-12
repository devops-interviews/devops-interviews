# Job Failure

> **Company:** RedHat | **Difficulty:** Easy

---

#### **Scenario**

A Job manifest at `/home/interview/fail-job.yaml` is failing with a non-zero exit status. The Job has limited retries configured.

#### **Task**

Fix the Job so it completes successfully.

| Property | Value |
|----------|-------|
| Namespace | `batch` |
| Job name | `fail-job` |
| backoffLimit | `1` |
| Command | `echo 'Success'; exit 0` |
