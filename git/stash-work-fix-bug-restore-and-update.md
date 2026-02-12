# Stash Work Fix Bug Restore and Update

> **Company:** IBM | **Difficulty:** Medium

---

#### **Scenario**

Uncommitted changes on `feature-ui` prevent you from switching branches to fix a critical bug on `main`.

#### **Task**

Stash local changes to clean the working directory with message `WIP: UI improvements`. Switch to a new branch `hotfix-auth` to implement the fix, then merge it into `main`. Finally, rebase `feature-ui` against the updated `main` and restore your stashed changes.

Changes in hotfix-auth branch are below:

```sh
echo  "Fixing critical bug" >> src/auth.js
git commit -m "Fix critical authentication bug"
```

#### **Example**

```
# Before (Switch blocked)
error: Your local changes to the following files would be overwritten by checkout:
        src/ui.js
Please commit your changes or stash them before you switch branches.

# After (Updated and Restored)
$ git log --oneline -1 main
a1b2c3d Fix critical authentication bug
$ git status
On branch feature-ui
Changes not staged for commit:
  modified:   src/ui.js
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/stash-work-fix-bug-restore-and-update)
