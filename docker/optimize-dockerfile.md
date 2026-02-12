# Optimize Dockerfile

> **Company:** Shopify | **Difficulty:** Medium

---

#### **Scenario**

A Dockerfile at `/home/interview/Dockerfile` successfully builds a Go application, but the resulting Docker image is over 800MB in size due to including the full Go toolchain, build dependencies, and source code. Production images must be under 200MB.

#### **Task**

Rewrite the Dockerfile using a multi-stage build pattern to separate the build environment from the runtime environment. Use `Alpine` as the base image for the final runtime stage, ensure only the compiled binary and necessary runtime dependencies are copied to the final stage, build the optimized image with the tag `myapp:fixed`, and verify the final image size is below 200MB while maintaining full functionality.

#### **Example**

```
# Before (bloated image)

REPOSITORY    TAG       SIZE
myapp         original  550MB
```

```
# After (optimized multi-stage build)

REPOSITORY    TAG       SIZE
myapp         fixed     45.3MB
```
