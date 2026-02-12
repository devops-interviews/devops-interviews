# Fix Inode Exhaustion Issue

> **Company:** DeutscheBank | **Difficulty:** Medium

---

#### Scenario:

Your server cannot create new files. Commands like `touch` fail with "No space left on device" errors, but `df -h` shows plenty of free disk space. The filesystem has exhausted available inodes.

#### Task:

Save inode usage to `/home/interview/inode_usage.txt`, find which directory contains excessive files, save the problematic directory path to `/home/interview/problem_directory.txt`, clean up the files, and verify the fix.

#### **Example**

**File: /home/interview/inode_usage.txt**
```
Filesystem            Inodes   IUsed   IFree IUse% Mounted on
/dev/sda1            6553600 6553600       0  100% /
/dev/sdb1            3276800  125000 3151800    4% /data
```

**File: /home/interview/problem_directory.txt**
```
/var/spool/postfix/maildrop
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/fix-inode-exhaustion-issue)
