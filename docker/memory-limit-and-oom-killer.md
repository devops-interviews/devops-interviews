# Memory Limit and OOM Killer

> **Company:** DeliveryHero | **Difficulty:** Medium

---

#### **Scenario**

A container named `mem_test` running from image `myapp:mem` contains a memory stress script at `/app/stress_memory.sh`. Currently, the container runs with unbounded memory and can consume as much RAM as available on the host, preventing the OOM (Out of Memory) killer from terminating it even when it allocates excessive memory.

#### **Task**

Apply `100MB` memory limits to the container so that running the provided stress script causes the container to be OOM-killed. Stop the container, restart it with memory limits applied using the appropriate flags, run the stress script, and verify the container gets OOM-killed when the memory limit is exceeded by checking the OOM kill status.

_Note: The container `mem_test` and image `myapp:mem` with the stress script are already available.

#### **Example**

```
# Before (no memory limits)
$ docker inspect mem_test --format 'Memory: {{.HostConfig.Memory}}'
Memory: 0

$ docker inspect mem_test --format 'OOMKilled: {{.State.OOMKilled}}'
OOMKilled: false
```

```
# After (memory limits applied and stress script triggers OOM)
$ docker inspect mem_test --format 'Memory: {{.HostConfig.Memory}}'
Memory: 104857600

$ docker inspect mem_test --format 'OOMKilled: {{.State.OOMKilled}}'
OOMKilled: true

$ docker inspect mem_test --format 'ExitCode: {{.State.ExitCode}}'
ExitCode: 137
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/memory-limit-and-oom-killer)
