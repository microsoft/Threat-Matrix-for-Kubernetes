---
hide:
  - toc
  - footer
---

# Avoid using web-hosted manifest for Kubelet

!!! info inline end
    ID: MS-M9032<br>
    MITRE mitigation: -


Kubelet can deploy static pods by using manifests that are stored web accessible locations. If web-hosted manifest are not required, make sure that Kubelet does not run with `--manifest-url` argument.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9017](../techniques/Static%20Pods.md)|Static Pods|Avoid using web-hosted manifest for Kubelet.|
