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

If the Kubernetes cluster is deployed in the cloud, in some cases attackers can leverage their access to a single container to get access to other cloud resources outside the cluster. For example, AKS uses several managed identities that are attached to the nodes, for the cluster operation. Similar identities exist also in EKS and GKE (EC2 roles and IAM service accounts, respectively). By default, running pods can retrieve the identities which in some configurations have privileged permissions. Therefore, if attackers gain access to a running pod in the cluster, they can leverage the identities to access external cloud resources.

Also, AKS has an option to authenticate with Azure using a service principal. When this option is enabled, each node stores service principal credentials that are located in /etc/kubernetes/azure.json. AKS uses this service principal to create and manage Azure resources that are needed for the cluster operation. By default, the service principal has contributor permissions in the cluster’s Resource Group. Attackers who get access to this service principal file (by hostPath mount, for example) can use its credentials to access or modify the cloud resources.


## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9003](../mitigations/MS-M9003%20Adhere%20to%20least-privilege%20principle.md)|Adhere to least-privilege principle|Grant only necessary permission to the cloud identities.|
|[MS-M9018](../mitigations/MS-M9018%20Restricting%20cloud%20metadata%20API%20access.md)|Restrict the access of pods to IMDS|Restrict the access of pods to IMDS to restrict pods from getting access to cloud identities.|
|[MS-M9019](../mitigations/MS-M9019%20Allocate%20specific%20identities%20to%20pods.md)|Allocate specific identities to pods|Use dedicated allocated identities to pods|
|[MS-M9013](../mitigations/MS-M9013%20Restrict%20over%20permissive%20containers.md)|Restrict over permissive containers|Block mounting volumes with access to cloud credentials.|