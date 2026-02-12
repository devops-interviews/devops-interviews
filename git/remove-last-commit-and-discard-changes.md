# Remove Last Commit and Discard Changes

> **Company:** Gitlab | **Difficulty:** Easy

---

#### **Scenario**

You have created a commit locally that contains incorrect changes and you want to completely erase it from history.

#### **Task**

Navigate to `/home/interview/repo`. Remove the last commit entirely and discard all associated file changes.

#### **Example**

```bash
# Before (Bad commit exists)
$ git log --oneline -2
c3d4e5f (HEAD -> main) Bad commit - wrong changes
b2c3d4e Add feature implementation

# After (Clean history)
$ git log --oneline -2
b2c3d4e (HEAD -> main) Add feature implementation
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/remove-last-commit-and-discard-changes)
