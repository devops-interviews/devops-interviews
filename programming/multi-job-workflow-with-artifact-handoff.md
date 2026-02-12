# Multi-Job Workflow with Artifact Handoff

> **Company:** Anthropic | **Difficulty:** Medium

---

#### Scenario

A repository at `/home/interview/repo` contains a Node.js application with a test suite at `./run-tests.sh`. The development team needs a two-stage CI/CD pipeline where the first job runs tests and generates test results, and a second job downloads those results to create a summary report. The repository has upload-artifact and download-artifact actions available locally at `.github/actions/` for artifact management. A starter workflow file has been created at `.github/workflows/artifact-handoff.yml` with the basic structure.

#### Task

Navigate to `/home/interview/repo` and complete the GitHub Actions workflow at `.github/workflows/artifact-handoff.yml` that implements a two-job pipeline triggered on `pull_request` events using container images (`node:20-slim`):

1. Job A (test-job): Run the test suite and upload the test-results.txt file as an artifact named "test-results" using `./.github/actions/upload-artifact`
2. Job B (report-job): Download the test-results artifact using `./.github/actions/download-artifact`, verify it exists, count passed tests with `grep -c "PASS:"`, save the count to `summary.txt` in format "Total Passed Tests: X", and upload as "test-summary" artifact. Job B must depend on Job A using the "needs" keyword.

The workflow can be tested with: `./github-ci pull_request`
