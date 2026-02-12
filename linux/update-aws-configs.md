# Update AWS Configs

> **Company:** Stripe | **Difficulty:** Medium

---

#### **Scenario**

Each application environment (staging, dev, prod) has its own configuration file stored under `/etc/app/envs/`, and each file currently has `multi_az = false` and `availability_zone = "us-east-1a"`. Manually editing each file is error-prone and inefficient, so the change must be automated.

#### **Task**

Locate all `.conf` files under `/etc/app/envs/` across different environment subdirectories, update the `multi_az` setting from `false` to `true`, modify the `availability_zone` line to include two zones `"us-east-1a,us-east-1b"`, perform these edits in-place while preserving all other configuration values.

#### **Example**

```
# Before (single-AZ configuration)

region = "us-east-1"
availability_zone = "us-east-1a"
multi_az = false
```

```
# After (multi-AZ configuration enabled)

region = "us-east-1"
availability_zone = "us-east-1a,us-east-1b"
multi_az = true
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/update-aws-configs)
