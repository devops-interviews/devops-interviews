# Convert Remote from HTTPS to SSH

> **Company:** EPAM | **Difficulty:** Easy

---

#### Scenario:

You have a Git repository at `/home/interview/repo` where the remote **origin is currently configured with an HTTPS URL** (`https://github.com/user/repo.git`).

#### Task:

Change the remote URL from HTTPS to SSH and verify the connection.

#### **Example:**

```
# Before (using HTTPS)
$ git remote -v
origin  https://github.com/user/repo.git (fetch)
origin  https://github.com/user/repo.git (push)
```

```
# After (using SSH)
$ git remote -v
origin  git@github.com:user/repo.git (fetch)
origin  git@github.com:user/repo.git (push)
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/convert-remote-from-https-to-ssh)
