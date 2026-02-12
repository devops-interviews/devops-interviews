# Reusable Workflow with Input Parameters

> **Company:** Adobe | **Difficulty:** Medium

---

#### Scenario

A repository at `/home/interview/repo` contains multiple applications that share common build and test steps. The development team wants to eliminate code duplication across workflows by creating a centralized reusable workflow that can be called from different workflows with different parameters.

#### Task

Create two GitHub Actions workflows: a reusable workflow at `.github/workflows/shared-build.yml` that accepts an input parameter `app-name`, runs a build script `./build.sh` with the app name, and uploads a build artifact named `"build-{app-name}"`; and a caller workflow at `.github/workflows/deploy.yml` that triggers on push events, calls the reusable workflow with `app-name: "frontend"`, and uses container image (`node:20-slim`). You can test with: `./github-ci push`
