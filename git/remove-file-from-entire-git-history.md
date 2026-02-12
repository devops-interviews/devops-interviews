# Remove File from Entire Git History

> **Company:** Netflix | **Difficulty:** Medium

---

#### **Scenario**

A file named `secrets.env` containing sensitive credentials exists in the repository's commit history. You need to purge this file from the entire history.

#### **Task**

Navigate to `/home/interview/repo` and rewrite the commit history to permanently remove `secrets.env` from all commits.

#### **Example**

```bash
# Before (Sensitive data in history)
$ git log --all --oneline -- secrets.env
a1b2c3d Add secrets file

# After (Clean history)
$ git log --all --oneline -- secrets.env
(no output)
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/remove-file-from-entire-git-history)
