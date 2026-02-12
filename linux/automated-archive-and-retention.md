# Automated Archive and Retention

> **Company:** Microsoft | **Difficulty:** Hard

---

#### **Scenario**

Configuration files in `/etc` are at risk of being lost due to accidental changes or deletions, and there's currently no automated backup process in place.

#### **Task**

Write a shell script at `/usr/local/bin/backup_etc.sh` that accepts a target backup path (where files will be saved at) as a command-line argument, creates a compressed archive of `/etc` with the naming format `etc-backup-YYYY-MM-DD.tar.gz`, automatically removes backups older than 7 days, and exits with an error if no path is provided. Make the script executable and create a **cron job** to run it daily at **02:00 AM**, storing backups in `/backups/etc/` using `crontab` command. You can use https://crontab.guru for cronjob format.

Once script is created execute it `/usr/local/bin/backup_etc.sh /backups/etc/`

#### **Example**

```
# Before (no automated backups)

No backup script exists
/etc directory unprotected
Manual backups required
```

```
# After (automated backup system configured)

Backup script created and executable
Running without argument:
  Error: Backup directory path required

Running with argument creates timestamped backup:
  /backups/etc/etc-backup-2025-11-06.tar.gz

After 7 days of daily backups:
  etc-backup-2025-11-01.tar.gz (deleted - older than 7 days)
  etc-backup-2025-11-02.tar.gz (deleted - older than 7 days)
  etc-backup-2025-11-03.tar.gz
  etc-backup-2025-11-04.tar.gz
  etc-backup-2025-11-05.tar.gz
  etc-backup-2025-11-06.tar.gz
  etc-backup-2025-11-07.tar.gz
  etc-backup-2025-11-08.tar.gz
  etc-backup-2025-11-09.tar.gz

Cron job configured: runs daily at 02:00 AM
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/automated-archive-and-retention)
