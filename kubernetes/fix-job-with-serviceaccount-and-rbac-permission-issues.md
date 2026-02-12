# Fix Job With ServiceAccount and RBAC Permission Issues

> **Company:** SAP | **Difficulty:** Medium

---

#### **Scenario**

You have a Kubernetes cluster where a job named `data-loader` in namespace `ops` **fails with permission denied** when calling the Kubernetes API. The job manifest file is located at `/home/interview/data-loader-job.yaml`.

#### **Task**

Fix the RBAC configuration and job specification so the job can successfully access the Kubernetes API to get and list pods.

#### **Example**

```bash
# Before (job fails)
$ kubectl get jobs -n ops
NAME          COMPLETIONS   DURATION   AGE
data-loader   0/1           2m         2m
```

```bash
# After (job completes)
$ kubectl get jobs -n ops
NAME          COMPLETIONS   DURATION   AGE
data-loader   1/1           15s        30s
```
