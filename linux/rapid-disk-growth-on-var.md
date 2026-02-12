# Rapid Disk Growth on Var

> **Company:** Google | **Difficulty:** Hard

---

#### **Scenario**

Disk usage on the `/var` partition is at 92% and increasing rapidly. You need to identify the largest files consuming space and determine if they're actively used by processes or need log rotation.

#### **Task**

Find the 10 largest files under `/var` and save them to `/home/devops/largest_var_files.txt`, check which processes are using these files and save results to `/home/devops/file_processes.txt`, and verify log rotation configuration for any log files found, saving results to `/home/devops/logrotate_status.txt`.

#### **Example**

```
# File: /home/devops/largest_var_files.txt
2.3G    /var/log/mysql/mysql-slow.log
1.8G    /var/lib/docker/overlay2/abc123/diff/app/data.db
1.3G    /var/log/nginx/access.log
891M    /var/cache/apt/archives/linux-image-generic.deb
655M    /var/log/syslog.1
450M    /var/log/myapp/app.log
...
```

```
# File: /home/devops/file_processes.txt
tail     44 root    3r   ... /var/log/mysql/sorted.log
tail     45 root    3r   ... /var/log/nginx/test.log
tail     46 root    3r   ... /var/log/hello.1
...
```

```
# File: /home/devops/logrotate_status.txt
/etc/logrotate.d/test:/var/log/test.log
/etc/logrotate.d/test:/var/log/hello.log
...
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/rapid-disk-growth-on-var)
