---
hide:
  - toc
  - footer
---

# Access Kubernetes Dasbhoard

!!! info inline end
    ID: ???<br>
    Tactic: [Discovery](../Discovery/index.md) <br>
    MITRE technique: [T1613](https://attack.mitre.org/techniques/T1613/)

The Kubernetes dashboard is a web-based UI that is used for monitoring and managing the Kubernetes cluster. The dashboard allows users to perform actions in the cluster using its service account (kubernetes-dashboard) with the permissions that are determined by the binding or cluster-binding for this service account. Attackers who gain access to a container in the cluster, can use its network access to the dashboard pod. Consequently, attackers may retrieve information about the various resources in the cluster using the dashboard’s identity.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|