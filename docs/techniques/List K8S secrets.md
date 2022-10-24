---
hide:
  - toc
  - footer
---

# List Kubernetes Secrets

!!! info inline end
    ID: MS-TA9025<br>
    Tactic: [Credential Access](../tactics/CredentialAccess/index.md) <br>
    MITRE technique: [T1552.007](https://attack.mitre.org/techniques/T1552/007/)

A Kubernetes secret is an object that lets users store and manage sensitive information, such as passwords and connection strings in the cluster. Secrets can be consumed by reference in the pod configuration. Attackers who have permissions to retrieve the secrets from the API server (by using the pod service account, for example) can access sensitive information that might include credentials to various services.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9003](../mitigations/MS-M9003%20Adhere%20to%20least-privilege%20principle.md)|Adhere to least-privilege principle|Limit users and service accounts access to Kubernetes secrets.|
|[MS-M9022](../mitigations/MS-M9022%20Use%20Managed%20Secret%20Store.md)|Use Managed Secret Store|Use cloud provider secret store to securely manage credentials in the cluster|
|[MS-M9023](../mitigations/MS-M9023%20Remove%20unused%20secrets%20from%20the%20cluster.md)|Remove unused secrets objects from the cluster|Remove unused secrets from the cluster.|
|[MS-M9024](../mitigations/MS-M9024%20Restrict%20access%20to%20etcd.md)|Restrict access to etcd|Restrict access to etcd.|