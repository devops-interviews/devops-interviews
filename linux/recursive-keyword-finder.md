# Recursive Keyword Finder

> **Company:** X | **Difficulty:** Easy

---

#### **Scenario**
Multiple applications write logs under `/var/log`, and you need to quickly check if any recent errors have been recorded.

#### **Task**
Search recursively under `/var/log` for all files ending with `.log`, print every line that contains the text `ERROR`, ensure the output includes both the filename and the matching line, and save the results to `/home/devops/error_logs.txt`.

#### **Example**
```
# Before (multiple log files scattered across directories)
/var/log/apache2/error.log
/var/log/apache2/access.log
/var/log/application.log
/var/log/mysql/error.log
/var/log/syslog
```
```
# After (ERROR lines found and saved to /home/devops/error_logs.txt)
/var/log/apache2/error.log:ERROR: Connection timeout to database server
/var/log/application.log:ERROR: Unable to write to cache directory
/var/log/mysql/error.log:ERROR: InnoDB: Cannot allocate memory for buffer pool
/var/log/syslog:ERROR: Disk quota exceeded for user appuser
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/recursive-keyword-finder)
