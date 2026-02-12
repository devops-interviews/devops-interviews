# Docker Volume Cross Platform Consistency

> **Company:** GitLab | **Difficulty:** Easy

---

#### Scenario:

You need to create a **Docker volume** named `myvol` and demonstrate **cross-platform consistency** - that data written from one container is readable by a different container using a different base image.

#### Task:

Create a Docker volume named `myvol`, mount it at `/data`, write a file `hello.txt` to it from an **`ubuntu:latest`** container, then read the same file from an **`alpine:latest`** container, ensuring the file exists at `/var/lib/docker/volumes/myvol/_data/hello.txt` on the host during validation.

#### **Example:**

```
# Writing from Ubuntu
ubuntu@container:/# echo "Hello from Ubuntu!" > /data/hello.txt
```
```
# Reading from Alpine
/ # cat /data/hello.txt
Hello from Ubuntu!
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/docker-volume-cross-platform-consistency)
