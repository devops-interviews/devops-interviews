# Custom Resource Definition Setup

> **Company:** ActivisionBlizzard | **Difficulty:** Medium

---

#### **Scenario**

You need to extend the Kubernetes API to support a proprietary resource type called "Widget".

#### **Task**

Create a CustomResourceDefinition named `widgets.mycompany.io`. Define the group as `mycompany.io` and the kind as `Widget` short name `wd` and with `served:true  storage:true` parameters. Specify the scope as `Namespaced` and define a version named `v1`. Create a Custom Resource instance of this type named `sample-widget` in the `extensions` namespace. Verify that the API accepts the new resource and that you can list it.

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/custom-resource-definition-setup)
