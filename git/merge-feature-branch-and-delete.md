# Merge Feature Branch and Delete

> **Company:** Expedia | **Difficulty:** Easy

---

#### Scenario:

You have a Git repository at `/home/interview/repo` where you've completed work on the `feature-login` branch. The feature is ready to be integrated into the `main` branch.

#### Task:

Merge feature-login into main and delete the feature branch in `/home/interview/repo`.

#### **Example:**

```
# Before (feature branch exists)
$ git branch
  feature-login
* main
$ git log --oneline -1 feature-login
d4e5f6a Add login validation
```

```
# After (feature merged and branch deleted)
$ git log --oneline -1 main
d4e5f6a Add login validation
$ git branch
* main
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/merge-feature-branch-and-delete)
