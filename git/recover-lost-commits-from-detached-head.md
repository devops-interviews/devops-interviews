# Recover Lost Commits from Detached Head

> **Company:** Kayak | **Difficulty:** Medium

---

#### Scenario:

You have a Git repository at `/home/interview/repo` where you were in a detached HEAD state, made 3 commits, then switched back to the `main` branch. Those 3 commits are now unreachable and appear to be lost since no branch references them.

#### Task:

Navigate to the repository at `/home/interview/repo`, check the reflog to locate the lost commits from the detached HEAD state, create a new branch called `recovered-work` pointing to those commits.

#### **Example:**

```
# Before (commits lost, only main visible)
$ git log --oneline -3
c3d4e5f Main branch work
b2c3d4e Second commit
a1b2c3d Initial commit
$ git branch
* main
```

```
# After (commits recovered in new branch)
$ git branch
* main
  recovered-work
$ git log recovered-work --oneline -3
f6a7b8c Third detached commit
e5f6a7b Second detached commit
d4e5f6a First detached commit
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/recover-lost-commits-from-detached-head)
