---
hide:
  - toc
  - footer
---

# Exposed Dashboard

!!! info inline end
    ID: ???<br>
    Tactic: [Initial Access](../InitialAccess/index.md), [Lateral Movement](../LateralMovement/index.md) <br>
    MITRE technique: [T1133](https://attack.mitre.org/techniques/T1133/)

The Kubernetes dashboard is a web-based user interface that enables monitoring and managing a Kubernetes cluster. By default, the dashboard exposes an internal endpoint (ClusterIP service). If the dashboard is exposed externally, it can allow unauthenticated remote management of the cluster.

Attackers who have access to the Kubernetes dashboard may manage the cluster resources and also run their code on the various containers in the cluster using the built-in “exec” capability of the dashboard.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|