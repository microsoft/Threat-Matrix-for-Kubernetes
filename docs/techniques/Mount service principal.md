---
hide:
  - toc
  - footer
---

# Mount Service Principal

!!! info inline end
    ID: ???<br>
    Tactic: [Credential Access](../CredentialAccess/index.md) <br>
    MITRE technique: [T1552.001](https://attack.mitre.org/techniques/T1552/001/)

When the cluster is deployed in the cloud, in some cases attackers can leverage their access to a container in the cluster to gain cloud credentials. For example, in AKS each node contains service principal credential.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|