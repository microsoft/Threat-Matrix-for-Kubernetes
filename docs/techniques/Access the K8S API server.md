---
hide:
  - toc
  - footer
---

# Access Kubernetes API server

!!! info inline end
    ID: MS-TA9029<br>
    Tactic: [Discovery](../tactics/Discovery/index.md) <br>
    MITRE technique: [T1613](https://attack.mitre.org/techniques/T1613/)

The Kubernetes API server is the gateway to the cluster. Actions in the cluster are performed by sending various requests to the RESTful API. The status of the cluster, which includes all the components that are deployed on it, can be retrieved by the API server. Attackers may send API requests to probe the cluster and get information about containers, secrets, and other resources in the cluster.

In addition, the Kubernetes API server can also be used to query information about Role Based Access (RBAC) information such as Roles, ClusterRoles, RoleBinding, ClusterRoleBinding and Service Accounts. Attacker may use this information to discover permissions and access associated with Service Accounts in the cluster and use this information to progress towards its attack objectives.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9003](../mitigations/MS-M9003%20Adhere%20to%20least-privilege%20principle.md)|Adhere to least-privilege principle|Configure the Kubernetes RBAC such as each service account has only the minimal necessary permissions for the application’s functionality.|
|[MS-M9002](../mitigations/MS-M9002%20Restrict%20access%20to%20the%20API%20server%20using%20IP%20firewall.md)|Restrict access to the API server using IP firewall|Restrict access of cloud accounts to API server from trusted IP addresses only.|
