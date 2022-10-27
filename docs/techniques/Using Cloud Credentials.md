---
hide:
  - toc
  - footer
---

# Using Cloud Credentials

!!! info inline end
    ID: MS-TA9001<br>
    Tactic: [Initial Access](../tactics/InitialAccess/index.md) <br>
    MITRE technique: [T1078.004](https://attack.mitre.org/techniques/T1078/004/)

In cases where the Kubernetes cluster is deployed in a public cloud (e.g., AKS in Azure, GKE in GCP, or EKS in AWS), compromised cloud credential can lead to cluster takeover. Attackers who have access to the cloud account credentials can get access to the cluster’s management layer.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9001](../mitigations/MS-M9001%20Multi-factor%20Authentication.md)|Multi-factor Authentication|Use multi-factor authentication for cloud accounts which can be elevated to access Kubernetes clusters in that cloud.|
|[MS-M9002](../mitigations/MS-M9002%20Restrict%20access%20to%20the%20API%20server%20using%20IP%20firewall.md)|Restrict access to the API server using IP firewall|Restrict access of cloud accounts to API server from trusted IP addresses only.|
|[MS-M9003](../mitigations/MS-M9003%20Adhere%20to%20least-privilege%20principle.md)|Adhere to least-privilege principle|Limit RBAC privileges in the cloud account to retrieve access credentials to managed Kubernetes clusters.|