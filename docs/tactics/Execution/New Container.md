---
hide:
  - toc
  - footer
---

# New Container

!!! info inline end
    ID: ???<br>
    Tactic: [Execution](../Execution/index.md) <br>
    MITRE technique: [T1610](https://attack.mitre.org/techniques/T1610/)

Attackers may attempt to run their code in the cluster by deploying a container. Attackers who have permissions to deploy a pod or a controller in the cluster (such as DaemonSet \ ReplicaSet\ Deployment) can create a new resource for running their code.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|