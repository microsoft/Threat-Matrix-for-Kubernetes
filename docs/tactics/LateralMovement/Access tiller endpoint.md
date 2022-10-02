---
hide:
  - toc
  - footer
---

# Access tiller endpoint

!!! info inline end
    ID: ???<br>
    Tactic: [Lateral Movement](../LateralMovement/index.md) <br>
    MITRE technique: [T1133](https://attack.mitre.org/techniques/T1133/)

Helm is a popular package manager for Kubernetes maintained by CNCF. Tiller is the server-side component of Helm up to version 2.

Tiller exposes internal gRPC endpoint in the cluster, listens to port 44134. By default, this endpoint does not require authentication. Attackers may run code on any container that is accessible to the tiller’s service and perform actions in the cluster, using the tiller’s service account, which often has high privileges.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|