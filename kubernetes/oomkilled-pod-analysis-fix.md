# OOMKilled Pod Analysis Fix

> **Company:** Accenture | **Difficulty:** Medium

---

#### **Scenario**

A memory-intensive application named `oom-demo` is repeatedly crashing. The pod status shows `CrashLoopBackOff`, but you need to confirm the underlying cause is an "Out Of Memory" (OOM) error and fix it by increasing the memory limit.

#### **Task**

Inspect the existing pod `oom-demo` in the `apps` namespace. Confirm the termination reason is `OOMKilled`. Update the pod definition to increase the memory limit from `20Mi` to `100Mi`. Verify the pod stabilizes and enters the `Running` state.

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/oomkilled-pod-analysis-fix)
