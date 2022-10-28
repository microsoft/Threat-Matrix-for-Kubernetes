---
hide:
  - toc
  - footer
---

# Use managed secret store

!!! info inline end
    ID: MS-M9022<br>
    MITRE mitigation: [M1029](https://attack.mitre.org/mitigations/M1029/)


Use cloud secret store, such as Azure Key Vault, to securely store secrets that are used by the workloads in the cluster. This allows cloud-level management of the secret which includes permission management, expiration management, secret rotation, auditing, etc. The integration of cloud secret stores with Kubernetes is done by using Secrets Store CSI Driver, which is implemented by all major cloud providers.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9025](../techniques/List%20K8S%20secrets.md)|List Kubernetes secrets|Use cloud provider secret store to securely manage credentials in the cluster|
|[MS-TA9027](../techniques/Application%20credentials%20in%20configuration%20files.md)|Application credentials in configuration files|Store secrets securely in managed secret stores|
