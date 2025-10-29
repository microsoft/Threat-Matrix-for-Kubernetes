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
|[MS-TA9042](../techniques/Excessive%20operator%20permissions.md)|Excessive operator permissions|Ablock excessive or unintended RBAC permissions.|
