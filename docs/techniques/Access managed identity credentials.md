---
hide:
  - toc
  - footer
---

# Access Managed Identity credentials

!!! info inline end
    ID: MS-TA9028<br>
    Tactic: [Credential Access](../tactics/CredentialAccess/index.md) <br>
    MITRE technique: [T1552.005](https://attack.mitre.org/techniques/T1552/005/)

Managed identities are identities that are managed by the cloud provider and can be allocated to cloud resources, such as virtual machines. Those identities are used to authenticate with cloud services. The identity’s secret is fully managed by the cloud provider, which eliminates the need to manage the credentials. Applications can obtain the identity’s token by accessing the Instance Metadata Service (IMDS). Attackers who get access to a Kubernetes pod can leverage their access to the IMDS endpoint to get the managed identity’s token. With a token, the attackers can access cloud resources.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9018](../mitigations/MS-M9018%20Restricting%20cloud%20metadata%20API%20access.md)|Restricting cloud metadata API access|Restrict the access of pods to IMDS|
|[MS-M9019](../mitigations/MS-M9019%20Allocate%20specific%20identities%20to%20pods.md)|Allocate specific identities to pods|Allocate specific identities to pods.|