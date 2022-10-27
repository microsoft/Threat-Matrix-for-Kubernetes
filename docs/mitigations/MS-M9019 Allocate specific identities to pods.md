---
hide:
  - toc
  - footer
---

# Allocate specific identities to pods

!!! info inline end
    ID: MS-M9019<br>
    MITRE mitigation: -


When needed, allocate dedicated cloud identity per pod with minimal permissions, instead of inheriting the node’s cloud identity. This prevents other pods from accessing cloud identities that are not necessary for their operation. The features that implement this separation are: Azure AD Pod Identity (AKS), Azure AD Workload identity (AKS), IRSA (EKS) and GCP Workload Identity (GCP).


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9020](../techniques/Access%20cloud%20resources.md)|Access cloud resources|Use dedicated allocated identities to pods|
|[MS-TA9028](../techniques/Access%20managed%20identity%20credentials.md)|Access Managed Identity credentials|Allocate specific identities to pods.|