# Purge Empty Folders

> **Company:** CrowdStrike | **Difficulty:** Easy

---

#### **Scenario**

The `/tmp` directory has accumulated numerous leftover folders from previous application runs and temporary scripts. Many of these directories are now empty and can be safely removed.

#### **Task**

Write a command or short script that searches through `/tmp`, finds all empty directories recursively, and deletes them without affecting any directories that contain files or subdirectories.

#### **Example**

```
# Before (empty directories present)

/tmp/old_build_cache/
/tmp/session_temp_1234/
/tmp/extract_workspace/
/tmp/app_tmp_5678/
/tmp/active_project/file.txt
```

```
# After (empty directories removed)

/tmp/active_project/file.txt
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/purge-empty-folders)
