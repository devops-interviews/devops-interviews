# CRD Schema Validation

> **Company:** RedHat | **Difficulty:** Hard

---

#### **Scenario**

You manage a CustomResourceDefinition (CRD) for "Widgets". Currently, the API allows users to create widgets with missing or invalid configuration, which causes the controller to crash.

#### **Task**

Modify the existing `widgets.mycompany.io` CRD to enforce a schema. Require the field `spec.size` to be present. Restrict `spec.size` to be an `integer` with a minimum value of `1`. Attempt to create a custom resource named `bad-widget` (provided in the file `bad-widget.yaml`) that is missing the size field. Verify that the creation fails and the resource is **not** created.

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/crd-schema-validation)
