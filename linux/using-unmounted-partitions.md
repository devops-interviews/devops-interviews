# Using Unmounted Partitions

> **Company:** RedHat | **Difficulty:** Medium

---

#### **Scenario**

The server has unmounted partitions that are not being used and could be utilized for additional storage.

#### **Task**

Identify unmounted partitions that are safe to use (avoiding system-critical partitions like `/`, `/boot`, `/boot/efi`, or swap), create an ext4 filesystem on one with a label `data_extra`, mount it at `/mnt/test`, and verify it's accessible.

#### **Example**

```
# Before (unmounted partition unused)
Block devices scanned, unmounted partitions found
loop0p2: 20GB unmounted, no filesystem
```

```
# After (partition formatted and mounted)
Filesystem created: ext4 with label=data_extra on /dev/loop0p2
Mounted at: /mnt/test
/dev/loop0p2 on /mnt/test type ext4 (rw,relatime)
Partition ready for use
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/using-unmounted-partitions)
