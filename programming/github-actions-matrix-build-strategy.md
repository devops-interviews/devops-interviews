# GitHub Actions Matrix Build Strategy

> **Company:** Spotify | **Difficulty:** Medium

---

#### Scenario

A repository at `/home/interview/repo` contains a Node.js application with a test suite at `./run-tests.sh`. The application needs to be tested across multiple Node.js versions (18, 20, and 22) to ensure compatibility, but currently has no automated testing configured. A starter workflow file has been created at `.github/workflows/pr-tests.yml` with the basic structure. The repository has the upload-artifact action available locally at `.github/actions/upload-artifact` for artifact management.

#### Task

Navigate to `/home/interview/repo` and complete the GitHub Actions workflow at `.github/workflows/pr-tests.yml` that runs the test suite across Node.js versions 18, 20, and 22 using a matrix strategy. Each matrix job should create a `node-version.txt` artifact containing its Node.js version number. The workflow should execute on pull requests. The workflow can be tested with `./github-ci pull_request` and artifacts will be available in `/tmp/github-artifacts/1/` for verification.

***Important**: Use container images (`node:${{ matrix.node-version }}-slim`) instead of setup-node actions to configure Node.js versions.*
