# Nginx Rate Limit Calculation

> **Company:** Cloudflare | **Difficulty:** Hard

---

#### **Scenario**

Your Nginx web server has recently experienced performance issues caused by excessive traffic from a few aggressive clients. You've decided to enable rate limiting based on the recent traffic pattern. To determine the proper limit, you first need to analyze request frequency.

#### **Task**

Find the top 3 client IPs by number of requests from `/var/log/nginx/access.log`, calculate the rate limit using the formula `(sum of top 3 IP request counts / 3) * 0.8`, write this value into `/etc/nginx/nginx.conf` as `limit_req_zone $binary_remote_addr zone=app_limit:10m rate=<rate_limit>r/s;`, and verify the configuration with `nginx -t`.

#### **Example**

```
# Before (no rate limiting configured)

Access log contains thousands of requests from various IPs
No rate limit configured in nginx.conf
Need to analyze traffic and set appropriate limit
```

```
# After (rate limit calculated and configured)

Top 3 IPs analyzed: 4523, 3891, 3456 requests
Rate limit calculated: 7896 r/s
Configuration updated and validated successfully
nginx -t: syntax ok, test successful
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/nginx-rate-limit-calculation)
