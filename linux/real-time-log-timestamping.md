# Real-Time Log Timestamping

> **Company:** Adobe | **Difficulty:** Medium

---

#### **Scenario**

You're troubleshooting a service that produces untagged log output when run manually, making it difficult to analyze timing and sequence of events.

#### **Task**

Create a command that reads from standard input line by line and appends the current timestamp to the end of each line as it's read. Test it interactively by piping output to verify it works, then save the solution to a shell script at `/usr/local/bin/timestamp.sh` and make it executable so it can be used in any pipeline.

#### **Example**

```
# Before (untagged log output)

Application started
Processing request #1234
Database connection established
Request completed
```

```
# After (timestamped in real-time)

Application started - 2025-11-06 15:30:45
Processing request #1234 - 2025-11-06 15:30:46
Database connection established - 2025-11-06 15:30:47
Request completed - 2025-11-06 15:30:48
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/real-time-log-timestamping)
