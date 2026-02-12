# Docker Multi Architecture Image

> **Company:** Accenture | **Difficulty:** Easy

---

#### Scenario:

You have a Dockerfile at `/home/interview/Dockerfile` that needs to be built for multiple architectures to support different hardware platforms. Currently, building with `docker build` only creates images for the **host architecture**.

#### Task:

Configure Docker Buildx instance named `multiarch` with `buildx create` to build the image for both amd64 and arm64 architectures using  Push the multi-arch manifest to `localhost:5000/myapp:multi`.

#### **Example:**

```
Building for linux/amd64 only
```
```
Building for linux/amd64, linux/arm64
Pushing manifest list to localhost:5000/myapp:multi
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/docker-multi-architecture-image)
