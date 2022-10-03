---
hide:
  - toc
  - footer
---

# Kubeconfig file

!!! info inline end
    ID: MS-TA9003<br>
    Tactic: [Initial Access](../tactics/InitialAccess/index.md) <br>
    MITRE technique: 

The kubeconfig file, also used by kubectl, contains details about Kubernetes clusters including their location and credentials. If the cluster is hosted as a cloud service (such as AKS or GKE), this file is downloaded to the client via cloud commands (e.g., “az aks get-credential” for AKS or “gcloud container clusters get-credentials” for GKE).


If attackers get access to this file, for instance via a compromised client, they can use it for accessing the clusters.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|