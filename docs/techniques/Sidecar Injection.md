---
hide:
  - toc
  - footer
---

# Sidecar injection

!!! info inline end
    ID: MS-TA9011<br>
    Tactic: [Execution](../tactics/Execution/index.md) <br>
    MITRE technique: [T1610](https://attack.mitre.org/techniques/T1610/)

A Kubernetes Pod is a group of one or more containers with shared storage and network resources. Sidecar container is a term that is used to describe an additional container that resides alongside the main container. For example, service-mesh proxies are operating as sidecars in the applications’ pods. Attackers can run their code and hide their activity by injecting a sidecar container to a legitimate pod in the cluster instead of running their own separated pod in the cluster.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9003](../mitigations/MS-M9003%20Adhere%20to%20least-privilege%20principle.md)|Adhere to least-privilege principle|Prevent unnecessary users and service accounts from creating new pods and controllers.|
|[MS-M9013](../mitigations/MS-M9013%20Limit%20Container%20Capabilities.md)|Limit Container Capabilities|Restrict over permissive containers in the cluster using admission controller.|
|[MS-M9005.003](../mitigations/MS-M9005/MS-M9005.003%20Gate%20images%20deployed%20to%20Kubenertes%20cluster.md)|Gate images deployed to Kubernetes cluster|Restrict deployment of new containers from trusted supply chain|