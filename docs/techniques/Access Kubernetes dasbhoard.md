---
hide:
  - toc
  - footer
---

# Access Kubernetes Dashboard

!!! info inline end
    ID: MS-TA9032<br>
    Tactic: [Discovery](../tactics/Discovery/index.md) <br>
    MITRE technique: [T1613](https://attack.mitre.org/techniques/T1613/)

The Kubernetes dashboard is a web-based UI that is used for monitoring and managing the Kubernetes cluster. The dashboard allows users to perform actions in the cluster using its service account (kubernetes-dashboard) with the permissions that are determined by the binding or cluster-binding for this service account. Attackers who gain access to a container in the cluster, can use its network access to the dashboard pod. Consequently, attackers may retrieve information about the various resources in the cluster using the dashboard’s identity.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9008](../mitigations/MS-M9008%20Limit%20Access%20to%20Services%20Over%20Network.md)|Limit Access to Services Over Network|Avoid using Kubernetes dashboard if possible|
|[MS-M9014](../mitigations/MS-M9014%20Network%20Segmentation.md)|Network Segmentation|Restrict access to the Kubernetes dashboard service|