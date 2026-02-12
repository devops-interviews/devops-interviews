# Shallow Clone Limited to Latest Commit

> **Company:** Elastic | **Difficulty:** Easy

---

#### **Scenario**

A deployment pipeline is experiencing slow build times because it performs full history clones.

#### **Task**

Navigate to `/home/interview/workspace` and create a shallow clone of the repository (`file:///tmp/source-repo/repo.git`) named `shallow-repo`, restricted to the latest commit only.

#### **Example**

```bash
# Verify the clone is shallow (Has only 1 commit)
$ cd shallow-repo
$ git log --oneline
a1b2c3d (HEAD -> main, origin/main, origin/HEAD) Update deployment config
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/shallow-clone-limited-to-latest-commit)
