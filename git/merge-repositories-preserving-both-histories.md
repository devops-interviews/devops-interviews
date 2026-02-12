# Merge Repositories Preserving Both Histories

> **Company:** Zscaler | **Difficulty:** Medium

---

#### Scenario:

You have two separate Git repositories at `/home/interview/repo-a` (5 commits) and `/home/interview/repo-b` (4 commits) developed independently. Create a new monorepo at `/home/interview/monorepo` that combines both repositories into separate subdirectories using subtree (`project-a/` and `project-b/`) while preserving the full commit history from both repositories.

#### **Example:**

```
# Before (two separate repositories)
$ cd /home/interview/repo-a && git log --oneline | wc -l
5
$ cd /home/interview/repo-b && git log --oneline | wc -l
4
```

```
# After (combined monorepo with both histories)
$ cd /home/interview/monorepo && ls -la
project-a/  project-b/  .git/
$ git log --all --oneline | wc -l
12
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/merge-repositories-preserving-both-histories)
