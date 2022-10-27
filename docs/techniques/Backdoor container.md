---
hide:
  - toc
  - footer
---

# Backdoor Container

!!! info inline end
    ID: MS-TA9012<br>
    Tactic: [Persistence](../tactics/Persistence/index.md) <br>
    MITRE technique: [T1569](https://attack.mitre.org/techniques/T1569/)

Attackers run their malicious code in a container in the cluster. By using the Kubernetes controllers such as DaemonSets or Deployments, attackers can ensure that a constant number of containers run in one, or all, the nodes in the cluster.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9003](../mitigations/MS-M9003%20Adhere%20to%20least-privilege%20principle.md)|Adhere to least-privilege principle|Prevent unnecessary users and service accounts from creating new pods and controllers.|
|[MS-M9013](../mitigations/MS-M9013%20Limit%20Container%20Capabilities.md)|Limit Container Capabilities|Restrict over permissive containers in the cluster using admission controller.|
|[MS-M9005.003](../mitigations/MS-M9005/MS-M9005.003%20Gate%20images%20deployed%20to%20Kubenertes%20cluster.md)|Gate images deployed to Kubernetes cluster|Restrict deployment of new containers from trusted supply chain|