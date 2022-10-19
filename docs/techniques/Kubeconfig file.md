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
|[MS-M9003](../mitigations/MS-M9003%20Adhere%20to%20least-privilege%20principle.md)|Adhere to least-privilege principle|Limit privileges and actions that can be achieved by getting access to a kubeconfig file|
|[MS-M9002](../mitigations/MS-M9002%20Restrict%20access%20to%20the%20API%20server%20using%20IP%20firewall.md)|Restrict access to the API server using IP firewall|Restrict access to the API server from known IP addresses|
|[MS-M9006](../mitigations/MS-M9006%20Enable%20Just%20In%20Time%20access%20to%20API%20server.md)|Enable Just In Time access to API server|Enable JIT elevated access to API server to limit attack surface or impact.|
