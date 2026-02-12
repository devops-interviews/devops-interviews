# Fix Port Exhaustion for High Speed Scraper

> **Company:** X | **Difficulty:** Medium

---

#### **Scenario**

A `web-scraper` systemd service is running on this system, making continuous HTTP requests. The service has started experiencing connection failures - logs show HTTP status 000 errors, indicating connections cannot be established even though the network is functional and remote servers are accessible.

#### **Task**
Check the service status and logs to understand the failures, investigate the underlying cause, identify which system resource is exhausted, `apply the appropriate kernel configuration change`.

Once fix is applied you can test the connection with `curl -o /dev/null -s -w "HTTP Status: %{http_code}\n" http://example.com`

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/fix-port-exhaustion-for-high-speed-scraper)
