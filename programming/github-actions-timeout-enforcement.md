# GitHub Actions Timeout Enforcement

> **Company:** Bloomberg | **Difficulty:** Easy

---

#### Scenario

A repository at `/home/interview/repo` contains a deployment workflow that occasionally hangs due to network issues or unresponsive external services. Jobs must be automatically terminated if they exceed a time limit to prevent resource waste. A starter workflow file has been created at `.github/workflows/deploy.yml` with the basic structure.

#### Task

Navigate to `/home/interview/repo` and complete the GitHub Actions workflow at `.github/workflows/deploy.yml` that triggers on push events and enforces a job-level timeout of 2 minutes using `timeout-minutes: 2`. The deploy job should check out code and run `./scripts/long-running-task.sh`. The workflow can be tested with `./github-ci push`.
