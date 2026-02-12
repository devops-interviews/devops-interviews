# Checkout Single File from Another Branch

> **Company:** Twilio | **Difficulty:** Easy

---

#### **Scenario**

You are working on the `main` branch and need to update `config.json` with changes that currently exist only on the `feature-settings` branch, without switching your current context.

#### **Task**

Navigate to `/home/interview/repo` and retrieve the `config.json` file from the `feature-settings` branch into your current working directory.

#### **Example**

```bash
# Before (Old config on main)
$ cat config.json
{ "version": "1.0.0" }

# After (New config retrieved)
$ cat config.json
{ "version": "2.0.0" }
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/checkout-single-file-from-another-branch)
