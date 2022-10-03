---
hide:
  - toc
  - footer
---

# Container Service Account

!!! info inline end
    ID: MS-TA9016<br>
    Tactic: [Credential Access](../tactics/CredentialAccess/index.md), [Lateral Movement](../tactics/LateralMovement/index.md), [Persistence](../tactics/Persistence/index.md) <br>
    MITRE technique: [T1528](https://attack.mitre.org/techniques/T1528/)

Service account (SA) represents an application identity in Kubernetes. By default, a Service Account access token is mounted to every created pod in the cluster and containers in the pod can send requests to the Kubernetes API server using the Service Account credentials. Attackers who get access to a pod can access the Service Account token (located in `/var/run/secrets/kubernetes.io/serviceaccount/token`) and perform actions in the cluster, according to the Service Account permissions. If RBAC is not enabled, the Service Account has unlimited permissions in the cluster. If RBAC is enabled, its permissions are determined by the RoleBindings \ ClusterRoleBindings that are associated with it.

An attacker which get access to the Service Account token can also authenticate and access the Kubernetes API server from outside the cluster and maintain access to the cluster.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|