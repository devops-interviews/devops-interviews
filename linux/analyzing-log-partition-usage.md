# Analyzing Log Partition Usage

> **Company:** RedHat | **Difficulty:** Medium

---

#### **Scenario**

Log rotation has stopped working correctly, and you suspect that `/var/log` might be mounted on a different filesystem with limited space or incorrect mount options.

#### **Task**

Determine which filesystem or device `/var/log` is mounted on, including device name, mount point, filesystem type, size, and usage. Save the findings to `/home/devops/varlog_filesystem_info.txt` Optionally identify if this filesystem differs from `/` which could provide additional info on causes of log rotation or space issues.

#### **Example**
```
# After (filesystem identified and analyzed)

Filesystem      Size  Used Avail Use% Mounted on
/dev/sdb1       10G   9.8G  200M  98% /var/log

Mount details:
/dev/sdb1 on /var/log type ext4 (rw,relatime)
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/analyzing-log-partition-usage)
