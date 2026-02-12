# Fix Repository with Unrelated Histories

> **Company:** Zscaler | **Difficulty:** Medium

---

#### **Scenario:**

The repository at `/home/interview/repo` is in a broken state. Local and remote branches have diverged with **no common ancestor**. Consequently, `git push origin main` fails with a **non-fast-forward** error, and `git pull origin main` fails because the histories are **unrelated**.

#### **Task:**

Navigate to `/home/interview/repo`. **Merge and linearize** the unrelated histories (using rebase) to create a single commit sequence.

#### **Example:**

```bash
# Before (Broken)
$ git pull origin main
fatal: refusing to merge unrelated histories

# After (Fixed - Linear History)
$ git pull origin main
Already up to date.

$ git log --oneline --decorate
e8f9g0h (HEAD -> main, origin/main) Add local feature B
d7e8f9g Add local feature A
b5c6d7e Add remote config
a4b5c6d Remote initial commit
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/fix-repository-with-unrelated-histories)
