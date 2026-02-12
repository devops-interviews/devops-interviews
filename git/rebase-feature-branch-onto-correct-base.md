# Rebase Feature Branch Onto Correct Base

> **Company:** Samsung | **Difficulty:** Easy

---

#### **Scenario**

A Git repository at `/home/interview/repo` has a feature branch `feature-login` with several commits, but it was created from the wrong base branch.

#### **Task**

Rebase `feature-login` onto `develop` (it's currently based on `main`) while preserving all commits.

#### **Example**

```
# Before (feature branched from main)
* d7e8f9a (develop) Configure database settings
| * c2d3e4f (HEAD -> feature-login) Implement form validation
| * a9b0c1d Create login component
|/
* 3f4a5b6 (main) Initialize repository
```

```
# After (feature rebased onto develop)
* m8n9o0p (HEAD -> feature-login) Implement form validation
* k6l7m8n Create login component
* d7e8f9a (develop) Configure database settings
* 3f4a5b6 (main) Initialize repository
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/rebase-feature-branch-onto-correct-base)
