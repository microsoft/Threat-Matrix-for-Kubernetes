---
hide:
  - toc
  - footer
---

# List Kubernetes Secrets

!!! info inline end
    ID: ???<br>
    Tactic: [Credential Access](../CredentialAccess/index.md) <br>
    MITRE technique: [T1552.007](https://attack.mitre.org/techniques/T1552/007/)

A Kubernetes secret is an object that lets users store and manage sensitive information, such as passwords and connection strings in the cluster. Secrets can be consumed by reference in the pod configuration. Attackers who have permissions to retrieve the secrets from the API server (by using the pod service account, for example) can access sensitive information that might include credentials to various services.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|