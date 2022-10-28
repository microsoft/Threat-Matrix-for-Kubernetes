---
hide:
  - toc
  - footer
---

# Require strong authentication to services

!!! info inline end
    ID: MS-M9009<br>
    MITRE mitigation: -


Use strong authentication when exposing sensitive interfaces to the Internet. For example, attacks were observed against exposed Kubeflow and Argo workloads that were not configured to use OpenID Connect or other authentication methods.

Use strong authentication methods to the Kubernetes API that will prevent attackers from gaining access to the cluster even if valid credentials such as kubeconfig were achieved. For example, in AKS use AAD authentication instead of basic authentication. By using AAD authentication, a short-lived credential of the cluster is retrieved after authenticating to AAD.

Avoid using the read-only endpoint of Kubelet in port `10255`, which doesn’t require authentication. In newer version of managed clusters, this port is disabled.

## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9005](../techniques/Exposed%20sensitive%20interfaces.md)|Exposed sensitive interfaces|Require strong authentication to exposed services|
|[MS-TA9024](../techniques/Connect%20from%20Proxy%20server.md)|Connect from proxy server|Limit usage of kubeconfig authentication to the API server|
|[MS-TA9030](../techniques/Access%20Kubelet%20API.md)|Access Kubelet API|Avoid using the unsecured port 10255 for the Kubelet API|