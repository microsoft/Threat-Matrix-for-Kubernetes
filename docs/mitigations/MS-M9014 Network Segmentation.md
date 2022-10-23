---
hide:
  - toc
  - footer
---

# Network Segmentation

!!! info inline end
    ID: MS-M9014<br>
    MITRE mitigation: [M1030](https://attack.mitre.org/mitigations/M1030/)


Restrict inbound and outbound network traffic of the pods in the cluster. This includes inner-cluster communication as well as ingress\egress traffic to\from the cluster. Network Policies are a native K8s solution for networking restrictions in the cluster.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9009](../techniques/Application%20Exploit%20(RCE).md)|Application Exploit (RCE)|Limit network access to containers|
|[MS-TA9010](../techniques/SSH%20server%20running%20inside%20container.md)|SSH Server Running Inside Container|Limit network access to containers|