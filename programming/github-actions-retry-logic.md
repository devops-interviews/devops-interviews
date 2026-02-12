# GitHub Actions Retry Logic

> **Company:** Etsy | **Difficulty:** Easy

---

#### Scenario

A repository at `/home/interview/repo` contains a deployment workflow that occasionally fails due to transient issues. A deployment step running `./scripts/flaky-deploy.sh` fails on first attempt but succeeds on retry. The workflow needs automatic retry configuration to handle transient failures. A starter workflow file has been created at `.github/workflows/deploy.yml` with the basic structure.

#### Task

Navigate to `/home/interview/repo` and complete the GitHub Actions workflow at `.github/workflows/deploy.yml` that triggers on push events and implements automatic retry using the `nick-fields/retry@v3` action. The workflow should check out code and execute `./scripts/flaky-deploy.sh` with retry configuration `(timeout_minutes: 2, max_attempts: 3)`. The workflow can be tested with `./github-ci push`.
