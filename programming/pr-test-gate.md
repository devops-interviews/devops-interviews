# PR Test Gate

> **Company:** Adobe | **Difficulty:** Medium

---

#### Scenario

A repository at `/home/interview/repo` has a test suite located at `./run-tests.sh` but no automated testing on pull requests. Developers must manually run tests before merging, leading to inconsistent test coverage and occasional bugs in the main branch. A starter workflow file has been created at `.github/workflows/pr-tests.yml` with the basic structure. The repository already has the upload-artifact action available locally at `.github/actions/upload-artifact` for artifact management.

#### Task

Navigate to `/home/interview/repo` and complete the GitHub Actions workflow at `.github/workflows/pr-tests.yml` that triggers on pull request events, runs the test suite `./run-tests.sh`, and uploads the test results from `test-results.txt` as an artifact named `test-results` using `./.github/actions/upload-artifact`. The artifact upload should run even if tests fail using `if: always()`. Test with: `./github-ci pull_request` and artifacts will be available in `/tmp/github-artifacts/1/` for verification.
