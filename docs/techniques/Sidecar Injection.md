---
hide:
  - toc
  - footer
---

# Sidecar Injection

!!! info inline end
    ID: MS-TA9011<br>
    Tactic: [Execution](../tactics/Execution/index.md) <br>
    MITRE technique: [T1610](https://attack.mitre.org/techniques/T1610/)

A Kubernetes Pod is a group of one or more containers with shared storage and network resources. Sidecar container is a term that is used to describe an additional container that resides alongside the main container. For example, service-mesh proxies are operating as sidecars in the applications’ pods. Attackers can run their code and hide their activity by injecting a sidecar container to a legitimate pod in the cluster instead of running their own separated pod in the cluster.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|