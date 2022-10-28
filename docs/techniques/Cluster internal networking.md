---
hide:
  - toc
  - footer
---

# Cluster internal networking

!!! info inline end
    ID: MS-TA9034<br>
    Tactic: [Lateral Movement](../tactics/LateralMovement/index.md) <br>
    MITRE technique: [T1210](https://attack.mitre.org/techniques/T1210/)

Kubernetes networking behavior allows traffic between pods in the cluster as a default behavior. Attackers who gain access to a single container may use it for network reachability to another container in the cluster.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9014](../mitigations/MS-M9014%20Network%20Segmentation.md)|Network Segmentation|Provision pod network policies to restrict the traffic between pods|
|[MS-M9005](../mitigations/MS-M9005/index.md)|Image Assurance Policy|Avoid deployment of vulnerable applications to the cluster|