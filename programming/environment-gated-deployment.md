# Environment-Gated Deployment

> **Company:** Autodesk | **Difficulty:** Easy

---

#### Scenario

A repository at `/home/interview/repo` contains a deployment pipeline defined in `.github/workflows/deploy.yml`. Currently, the pipeline deploys to both Staging and Production environments automatically on every push. This is risky because unstable code could break the Production environment immediately.

#### Task

Modify the workflow to implement a gated deployment strategy. Configure the `staging` job to run automatically on push. Configure the `production` job to require manual approval using GitHub Environments. Assign the `production` job to an environment named `production`. Ensure the `production` job only runs after `staging` has successfully completed. The pipeline execution can be verified with `./github-ci push`.
