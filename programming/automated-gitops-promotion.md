# Automated GitOps Promotion

> **Company:** CapitalOne | **Difficulty:** Medium

---

#### Scenario

You are setting up a GitOps pipeline. `repo-a` contains the application source code, and `repo-b` contains the Kubernetes configuration (`values.yaml`).

When code is pushed to `repo-a`, the pipeline must:

1. Build a Docker image tagged with the **Short Git SHA**.
2. Automatically update `repo-b` to use this new image tag.

#### Task

Edit the existing workflow file at `/home/interview/repo-a/.github/workflows/promote.yml` to complete the pipeline.

1. **Calculate SHA:** Finish the step to extract the first 7 characters of `$GITHUB_SHA` into an environment variable named `SHORT_SHA`.
2. **Build:** Build a Docker image named `app` tagged with `${{ env.SHORT_SHA }}`.
3. **Checkout Infrastructure:** Configure the `checkout` step to clone `interview/repo-b` into a directory named `infra`.
4. **Promote:** Inside the `infra` directory:
   * Update `values.yaml` so that the `tag` key reflects the new `SHORT_SHA`.
   * Commit the change with the message: `Update tag to <SHORT_SHA>`.
