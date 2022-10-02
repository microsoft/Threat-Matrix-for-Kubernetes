---
hide:
  - toc
  - footer
---

# Access cloud resources

!!! info inline end
    ID: ???<br>
    Tactic: [Privilege Escalation](../tactics/PrivilegeEscalation/index.md), [Lateral Movement](../tactics/LateralMovement/index.md) <br>
    MITRE technique: [T1078.004](https://attack.mitre.org/techniques/T1078/004/)

If the Kubernetes cluster is deployed in the cloud, in some cases attackers can leverage their access to a single container in order to get access to other cloud resources outside the cluster. For example, in AKS each node contains service principal credential that is stored in /etc/kubernetes/azure.json. AKS uses this service principal to create and manage Azure resources that are needed for the cluster operation.

By default, the service principal has contributor permissions in the cluster’s Resource Group. Attackers who get access to this service principal file (by hostPath mount, for example) can use its credentials to access or modify the cloud resources.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|