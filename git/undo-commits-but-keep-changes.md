# Undo Commits but Keep Changes

> **Company:** CrowdStrike | **Difficulty:** Easy

---

#### Scenario:

You have a Git repository at `/home/interview/repo` with three recent commits on the `main` branch that were premature and need to be reorganized.

#### Task:

Undo the last three commits while keeping all changes in your working directory so you can recommit them properly.

#### **Example:**

```
# Before (three commits exist)
$ git log --oneline -4
d4e5f6a Third commit
c3d4e5f Second commit
b2c3d4e First commit
a1b2c3d Initial commit
```

```
# After (commits undone, changes kept)
$ git log --oneline -2
a1b2c3d Initial commit

$ git status
On branch main
Changes to be committed:
  modified:   file1.txt
  modified:   file2.txt
  modified:   file3.txt
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/undo-commits-but-keep-changes)
