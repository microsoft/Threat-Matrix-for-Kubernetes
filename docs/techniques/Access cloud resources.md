---
hide:
  - toc
  - footer
---

# Access cloud resources

!!! info inline end
    ID: MS-TA9020 <br>
    Tactic: [Privilege Escalation](../tactics/PrivilegeEscalation/index.md), [Lateral Movement](../tactics/LateralMovement/index.md) <br>
    MITRE technique: [T1078.004](https://attack.mitre.org/techniques/T1078/004/)

If the Kubernetes cluster is deployed in the cloud, in some cases attackers can leverage their access to a single container in order to get access to other cloud resources outside the cluster. For example, in AKS each node contains service principal credential that is stored in /etc/kubernetes/azure.json. AKS uses this service principal to create and manage Azure resources that are needed for the cluster operation.

By default, the service principal has contributor permissions in the cluster’s Resource Group. Attackers who get access to this service principal file (by hostPath mount, for example) can use its credentials to access or modify the cloud resources.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9003](../mitigations/MS-M9003%20Adhere%20to%20least-privilege%20principle.md)|Adhere to least-privilege principle|Grant only necessary permission to the cloud identities.|
|[MS-M9018](../mitigations/MS-M9018%20Restricting%20cloud%20metadata%20API%20access.md)|Restrict the access of pods to IMDS|Restrict the access of pods to IMDS to restrict pods from getting access to cloud identities.|
|[MS-M9019](../mitigations/MS-M9019%20Allocate%20specific%20identities%20to%20pods.md)|Allocate specific identities to pods|Use dedicated allocated identities to pods|
|[MS-M9013](../mitigations/MS-M9013%20Limit%20Container%20Capabilities.md)|Limit Container Capabilities|Block mounting volumes with access to cloud credentials.|