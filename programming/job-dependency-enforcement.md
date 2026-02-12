# Job Dependency Enforcement

> **Company:** Splunk | **Difficulty:** Medium

---

#### Scenario

A repository at `/home/interview/repo` contains a workflow file `.github/workflows/pipeline.yml`. The workflow currently defines three jobs: `lint`, `test`, and `build`. These jobs are configured to run in parallel without any dependencies.

#### Task

Update the pipeline to enforce a strict execution sequence. Configure the `test` job to depend on the successful completion of `lint`. Configure the `build` job to depend on the successful completion of `test`. The final execution order must be Lint → Test → Build. The pipeline execution can be verified with `./github-ci push`.
