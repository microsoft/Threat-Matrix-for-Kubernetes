---
hide:
  - toc
  - footer
---

# Enable Just In Time access to API server

!!! info inline end
    ID: MS-M9006<br>
    MITRE mitigation: -


Emplyoing Just In Time (JIT) elevated access to Kubernetes API server helps reduce the attack surface to the API server by compromised accounts by allowing access only at specific times, and through a goverened escalation  process. Enabling JIT access in Kubernetes is often done in together with OpenID authentication which includes processes and tools to manage JIT access. One example of such OpenID authentication is Azure Active Directory authentication to Kubernetes clusters. The JIT approval is performed in the cloud control-plane level. Therefore, even if attackers have access to an account credentials, their access to the cluster is limited.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9003](../techniques/Kubeconfig%20file.md)|Kubeconfig file|Enable JIT elevated access to API server to limit attack surface or impact.|