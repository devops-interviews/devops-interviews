# Automated Rollback on Deployment Failure with Values File Restoration

> **Company:** NVIDIA | **Difficulty:** Medium

---

#### Scenario

A repository at `/home/interview/deploy-repo` contains a `values.yaml` file tracking the current Docker image tag and a `deploy.sh` script that simulates production deployment. When deployments fail, the team must manually revert `values.yaml` to the previous working tag. An automated rollback mechanism is needed to detect failures and restore the last known-good tag with a commit by CI Bot. A starter workflow file has been created at `.github/workflows/deploy.yml` with the basic structure.

#### Task

Navigate to `/home/interview/deploy-repo` and complete the GitHub Actions workflow at `.github/workflows/deploy.yml` that triggers on push to main branch with two jobs: a deploy job that runs `./deploy.sh`, and a rollback job that depends on the deploy job, runs only when deployment fails, restores `values.yaml` to its state from the previous commit, and commits the change with author "CI Bot" ci-bot@example.com and message `chore: automatic rollback due to deployment failure`. Test with: `./github-ci push`
