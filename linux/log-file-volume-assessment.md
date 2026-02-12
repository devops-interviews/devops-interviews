# Log File Volume Assessment

> **Company:** JPMorgan | **Difficulty:** Easy

---

#### **Scenario**

The `/var` directory contains logs from multiple applications, and cleanup planning is needed. Some applications create their own subdirectories with nested log files.

#### **Task**

Find and count all files ending with the `.log` extension anywhere under `/var` including subdirectories, save the total count to `/home/devops/log_count.txt`, and use standard Linux commands to output only the total number of `.log` files found. Additionally, identify `.log` files **larger than 512 KB** and save the **count** to `/home/devops/large_log_count.txt`

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/log-file-volume-assessment)
