---
hide:
  - toc
  - footer
---

# Require Strong Authentication to Services

!!! info inline end
    ID: MS-M9009<br>
    MITRE mitigation: -


Use strong authentication when exposing sensitive interfaces to the Internet. For example, attacks were observed against exposed Kubeflow or Argo workloads that were not configured to use OpenID authentication.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9005](../techniques/Exposed%20sensitive%20interfaces.md)|Exposed Sensitive Interfaces|Require strong authentication to exposed services|