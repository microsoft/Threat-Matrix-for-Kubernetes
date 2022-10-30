---
hide:
  - toc
  - footer
---

# Exposed sensitive interfaces

!!! info inline end
    ID: MS-TA9005<br>
    Tactic: [Initial Access](../tactics/InitialAccess/index.md), [Discovery](../tactics/Discovery/index.md) <br>
    MITRE technique: [T1133](https://attack.mitre.org/techniques/T1133/)

Exposing a sensitive interface to the internet or within a cluster without strong authentication poses a security risk. Some popular cluster management services were not intended to be exposed to the internet, and therefore don’t require authentication by default. Thus, exposing such services to the internet allows unauthenticated access to a sensitive interface which might enable running code or deploying containers in the cluster by a malicious actor. Examples of such interfaces that were seen exploited include Apache NiFi, Kubeflow, Argo Workflows, Weave Scope, and the Kubernetes dashboard.

In addition, having such services exposed within the cluster network without strong authentication can also allow an attacker to collect information about other workloads deployed to the cluster.
The Kubernetes dashboard is an example of such a service that is used for monitoring and managing the Kubernetes cluster. The dashboard allows users to perform actions in the cluster using its service account (kubernetes-dashboard) with permissions that are determined by the binding or cluster-binding for this service account. Attackers who gain access to a container in the cluster, can use its network access to the dashboard pod. Consequently, attackers may retrieve information about the various resources in the cluster using the dashboard’s identity.


## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9008](../mitigations/MS-M9008%20Limit%20Access%20to%20Services%20Over%20Network.md)|Limit Access to Services Over Network|Limit access to sensitive interface over the Internet|
|[MS-M9009](../mitigations/MS-M9009%20Require%20Strong%20Authentication%20to%20Services.md)|Require Strong Authentication to Services|Require strong authentication to exposed services|
|[MS-M9014](../mitigations/MS-M9014%20Network%20Segmentation.md)|Network Segmentation|Restrict network access to the sensitive interfaces.|