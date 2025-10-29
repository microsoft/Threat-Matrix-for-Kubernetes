---
hide:
  - toc
  - footer
---

# Excessive operator permissions

!!! info inline end
    ID: MS-TA9042 <br>
    Tactic: [Privilege Escalation](../tactics/PrivilegeEscalation/index.md), [Impact](../tactics/Impact/index.md) 
    <br>
    MITRE technique: [T1078.004](https://attack.mitre.org/techniques/T1078/)

Kubernetes operators are custom controllers that extend the Kubernetes API to manage complex applications and their components. These operators frequently run with overly broad permissions that far exceed what's necessary for their operation. For instance, an operator designed to manage application deployments might be granted cluster-wide permissions including the ability to `get` and `list` secrets across all namespaces, or dangerous verbs like `escalate` and `bind` on roles and clusterroles. 

If attackers compromise an operator pod, they can exploit these excessive permissions to escalate privileges within the cluster. Many operators are granted overly permissive RBAC rules such as the ability to `get` and `list` secrets cluster-wide, which allows attackers to extract sensitive credentials, API tokens, and certificates. Additionally, operators with `escalate` or `bind` permissions on roles can grant themselves or other service accounts elevated privileges, effectively bypassing RBAC restrictions. Attackers who compromise operators with these permissions can use the operator's service account token to access secrets across the entire cluster or escalate to cluster-admin level access, potentially leading to complete cluster takeover.


## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9033](../mitigations/MS-M9018%20Admission%20policy%20enforcement%20access.md)|Admission policy enforcement|Use admission controllers to block excessive or unintended RBAC permissions |