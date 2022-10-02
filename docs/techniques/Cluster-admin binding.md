---
hide:
  - toc
  - footer
---

# Cluster-admin binding

!!! info inline end
    ID: ???<br>
    Tactic: [Privilege Escalation](../tactics/PrivilegeEscalation/index.md) <br>
    MITRE technique: [T1078.003](https://attack.mitre.org/techniques/T1078/003/)

Role-based access control (RBAC) is a key security feature in Kubernetes. RBAC can restrict the allowed actions of the various identities in the cluster. Cluster-admin is a built-in high privileged role in Kubernetes. Attackers who have permissions to create bindings and cluster-bindings in the cluster can create a binding to the cluster-admin ClusterRole or to other high privileges roles.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|