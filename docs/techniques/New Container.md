---
hide:
  - toc
  - footer
---

# New Container

!!! info inline end
    ID: MS-TA9008<br>
    Tactic: [Execution](../tactics/Execution/index.md) <br>
    MITRE technique: [T1610](https://attack.mitre.org/techniques/T1610/)

Attackers may attempt to run their code in the cluster by deploying a container. Attackers who have permissions to deploy a pod or a controller in the cluster (such as DaemonSet \ ReplicaSet\ Deployment) can create a new resource for running their code.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9003](../mitigations/MS-M9003%20Adhere%20to%20least-privilege%20principle.md)|Adhere to least-privilege principle|Prevent unnecessary users and service accounts from creating new pods and controllers.|
|[MS-M9013](../mitigations/MS-M9013%20Limit%20Container%20Capabilities.md)|Limit Container Capabilities|Restrict over permissive containers in the cluster using admission controller.|
|[MS-M9005.003](../mitigations/MS-M9005/MS-M9005.003%20Gate%20images%20deployed%20to%20Kubenertes%20cluster.md)|Gate images deployed to Kubenertes cluster|Restrict deployment of new containers from trusted supply chain|