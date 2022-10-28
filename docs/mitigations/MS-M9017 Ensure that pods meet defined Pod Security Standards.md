---
hide:
  - toc
  - footer
---

# Ensure that pods meet defined Pod Security Standards

!!! info inline end
    ID: MS-M9017<br>
    MITRE mitigation: -


The Pod Security Standards define three different policies to broadly cover the security spectrum. These policies are cumulative and range from highly-permissive to highly-restrictive. Decoupling policy definition from policy instantiation allows for a common understanding and consistent language of policies across clusters, independent of the underlying enforcement mechanism. At the same time, Kubernetes offers a built-in Pod Security admission controller to enforce the Pod Security Standards. Pod security restrictions are applied at the namespace level when pods are created.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9013](../techniques/Writable%20hostPath%20mount.md)|Writable hostPath mount|Use `Baseline` or `Restricted` pod security standards to prevent exploiting writable hostPath mount.|
|[MS-TA9018](../techniques/Privileged%20container.md)|Privileged container|Restrict privileged containers using pod security standards.|