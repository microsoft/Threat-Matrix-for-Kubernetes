---
hide:
  - toc
  - footer
---

# Mount service principal

!!! info inline end
    ID: MS-TA9026<br>
    Tactic: [Credential Access](../tactics/CredentialAccess/index.md) <br>
    MITRE technique: [T1552.001](https://attack.mitre.org/techniques/T1552/001/)

When the cluster is deployed in the cloud, in some cases attackers can leverage their access to a container in the cluster to gain cloud credentials. For example, in AKS each node contains service principal credential.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9013](../mitigations/MS-M9013%20Limit%20Container%20Capabilities.md)|Limit Container Capabilities|Block sensitive volume mounts using admission controller|
|[MS-M9003](../mitigations/MS-M9003%20Adhere%20to%20least-privilege%20principle.md)|Adhere to least-privilege principle|Grant minimal required permissions to service principals|