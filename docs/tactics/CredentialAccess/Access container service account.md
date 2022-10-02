---
hide:
  - toc
  - footer
---

# Access Container Service Account

!!! info inline end
    ID: ???<br>
    Tactic: [Credential Access](../CredentialAccess/index.md) <br>
    MITRE technique: [T1528](https://attack.mitre.org/techniques/T1528/)

Service account (SA) represents an application identity in Kubernetes. By default, an SA is mounted to every created pod in the cluster. Using the SA, containers in the pod can send requests to the Kubernetes API server. Attackers who get access to a pod can access the SA token (located in /var/run/secrets/kubernetes.io/serviceaccount/token) and perform actions in the cluster, according to the SA permissions. If RBAC is not enabled, the SA has unlimited permissions in the cluster. If RBAC is enabled, its permissions are determined by the RoleBindings \ ClusterRoleBindings that are associated with it.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|