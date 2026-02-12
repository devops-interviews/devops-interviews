# Track Forking Process Hierarchies

> **Company:** Splunk | **Difficulty:** Easy

---

#### **Scenario**

System resources are being consumed by an unusually large process tree. You need to identify the parent process with the most children and document its hierarchy.

#### **Task**

Identify the process tree with the highest number of child processes and save its hierarchy—including **PIDs** and **full command names (arguments)**—to: `/home/devops/process_tree_report.txt`.

Linux provides the `pstree` command to display full hierarchical process trees, including PIDs and command arguments.

#### **Example**

The file `/home/devops/process_tree_report.txt` should look similar to this:

```text
spawn_many_workers.sh,159 /home/devops/spawn_many_workers.sh
 ├─sleep,209 infinity
 ├─spawn_many_workers.sh,190 /home/devops/spawn_many_workers.sh
 │  └─sleep,220 60
 ├─spawn_many_workers.sh,191 /home/devops/spawn_many_workers.sh
 ...

```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/track-forking-process-hierarchies)
