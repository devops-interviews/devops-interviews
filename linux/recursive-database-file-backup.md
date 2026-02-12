# Recursive Database File Backup

> **Company:** GitLab | **Difficulty:** Easy

---

#### **Scenario**

Before performing a system-wide database schema migration, you've been asked to ensure that all existing `.db` files are safely backed up. These files may be scattered across multiple subdirectories, and simply renaming them isn't enough. You must create backup copies with the `.db.bak` extension, preserving directory structure and permissions.

#### **Task**

Recursively scan a given directory (`/opt/data/`) and create backup copies of all files ending with `.db`. Each backup should have the same name but with the `.bak` suffix added (e.g., `app.db` → `app.db.bak`) and remain in the same directory as the original file, ensuring the originals are left untouched.

#### **Example**

```
# Before (only original .db files exist)

/opt/data/apps/inventory.db
/opt/data/logs/session.db
/opt/data/config/settings.db
```

```
# After (backup copies created alongside originals)

/opt/data/apps/inventory.db
/opt/data/apps/inventory.db.bak
/opt/data/logs/session.db
/opt/data/logs/session.db.bak
/opt/data/config/settings.db
/opt/data/config/settings.db.bak
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/recursive-database-file-backup)
