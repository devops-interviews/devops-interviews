# Docker Image Tagging with Commit SHA

> **Company:** Microsoft | **Difficulty:** Medium

---

#### Scenario

A repository at `/home/interview/repo` contains a Dockerfile but no automated build process. Developers manually build Docker images without consistent tagging, making it difficult to track which image corresponds to which code version. A starter workflow file has been created at `.github/workflows/build.yml` with the basic structure.

#### Task

Navigate to `/home/interview/repo` and complete a GitHub Actions workflow at `.github/workflows/build.yml` that automatically builds a Docker image named `app` and tags it with the short commit SHA on every push to the main branch. The pipeline should ensure each commit produces a uniquely identifiable image. CI Pipeline can be executed and tested with `./github-ci push` command.
