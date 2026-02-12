# Handling Large Log Archives

> **Company:** Amazon | **Difficulty:** Easy

---

#### **Scenario**

During an incident investigation, you pulled a massive log export from `/var/log/app/access.log` that's several gigabytes in size. Your analysis tools and editors can't handle the entire file at once.
#### **Task**

You need to split it into smaller, more manageable chunks for parallel review. Create a directory `/tmp/log_parts/` to store the split files, split `/var/log/app/access.log` into smaller files containing 100 lines each, name the output files sequentially with the prefix `access_part_` (e.g., `access_part_aa`, `access_part_ab`, etc.), ensure the original log file remains untouched.

#### **Example**

```
# Before (single large log file)

/var/log/app/access.log: 375 lines, 2.5 GB
Cannot be opened by standard analysis tools
```

```
# After (log split into manageable chunks)

100 /tmp/log_parts/access_part_aa
100 /tmp/log_parts/access_part_ab
100 /tmp/log_parts/access_part_ac
 75 /tmp/log_parts/access_part_ad

375 total

Original file intact, 4 parts created for parallel analysis
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/handling-large-log-archives)
