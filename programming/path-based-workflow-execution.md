# Path-Based Workflow Execution

> **Company:** Coinbase | **Difficulty:** Medium

---

#### Scenario

A repository at `/home/interview/repo` contains a multi-component application with infrastructure code in the `/infra` directory and documentation in the `/docs` directory. Currently, the repository has no automated workflow configured with path-based filtering to run workflows only when specific files change. A starter workflow file has been created at `.github/workflows/infra-check.yml` with the basic structure. The repository has the upload-artifact action available locally at `.github/actions/upload-artifact` for artifact management.

#### Task

Navigate to `/home/interview/repo` and complete the GitHub Actions workflow at `.github/workflows/infra-check.yml` that runs only when files under the `/infra` directory change. The workflow should trigger on push events, use container image (`node:20-slim`), run a validation script at `./validate-infra.sh`, and create an artifact named "validation-report" containing `validation-result.txt` using `./.github/actions/upload-artifact`. The workflow can be tested with `./github-ci push` and artifacts will be available in `/tmp/github-artifacts/1/` for verification.
