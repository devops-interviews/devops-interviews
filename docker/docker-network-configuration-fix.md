# Docker Network Configuration Fix

> **Company:** Uber | **Difficulty:** Hard

---

#### Scenario:

You have created a **macvlan network** called `mymacvlan` to give containers their own MAC addresses on the physical network. However, containers `mac1` and `mac2` started on this network **cannot ping the host or the gateway** at `192.168.50.1`.

#### Task:

Correct the macvlan network configuration so that both `mac1` and `mac2` can successfully ping the gateway at `192.168.50.1` .

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/docker-network-configuration-fix)
