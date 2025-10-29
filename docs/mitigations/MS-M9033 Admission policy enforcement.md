---
hide:
  - toc
  - footer
---

# Admission policy enforcement

!!! info inline end
    ID: MS-M9033<br>
    MITRE mitigation: -


Use admission controllers such as OPA/Gatekeeper or Kyverno to prevent Operators or other components from gaining excessive or unintended access to Kubernetes resources. Enforce policies that validate RBAC rules and restrict creation or modification of objects that exceed the component’s intended privilege scope.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9017](../techniques/Static%20Pods.md)|Static pods|Avoid using web-hosted manifest for Kubelet.|
