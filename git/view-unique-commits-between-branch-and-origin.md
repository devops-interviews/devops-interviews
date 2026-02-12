# View Unique Commits Between Branch and Origin

> **Company:** EPAM | **Difficulty:** Easy

---

#### **Scenario**

A Git repository at `/home/interview/repo` has a `feature-api` branch that was created from `origin/main` some time ago. The branch has your commits plus merge commits from pulling updates, making it difficult to identify which commits are unique to your branch.

#### **Task**

Find commits unique to your branch compared to `origin/main`, exclude merge commits, write the unique commits to `/home/interview/unique-commits.txt`, and verify the file contains only the unique commits.

_Note: The remote repository `origin` is already configured._

#### **Example**

```
# After (unique commits saved to file)
File created with unique commits from feature-api branch
Merge commits excluded
Only commits not present in origin/main are listed

Example '/home/interview/unique-commits.txt' content:
"""
ree2ras Commit message
cji29nc Commit message
ch92uhd Commit message
"""
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/view-unique-commits-between-branch-and-origin)
