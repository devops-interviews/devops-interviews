# Sorted Log Aggregation

> **Company:** Airbnb | **Difficulty:** Easy

---

#### **Scenario**

You have a log file `/tmp/app_combined.log` with entries from multiple servers in mixed order. Each line contains: timestamp, hostname, and action.

#### **Task**

Sort `/tmp/app_combined.log` by timestamp (earliest first), then by hostname for identical timestamps. Save the output to `/tmp/app_sorted.log`.

#### **Example**

```
# Before (mixed order)
2025-12-18 14:23:45 api02 POST /users/create
2025-12-18 14:22:10 cache01 CACHE_MISS key=session_abc
2025-12-18 14:22:55 api01 GET /products/list
2025-12-18 14:22:10 db02 INSERT INTO orders VALUES
2025-12-18 14:24:12 cache01 CACHE_SET key=user_profile
```

```
# After (sorted by timestamp, then hostname)
2025-12-18 14:22:10 cache01 CACHE_MISS key=session_abc
2025-12-18 14:22:10 db02 INSERT INTO orders VALUES
2025-12-18 14:22:55 api01 GET /products/list
2025-12-18 14:23:45 api02 POST /users/create
2025-12-18 14:24:12 cache01 CACHE_SET key=user_profile
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/sorted-log-aggregation)
