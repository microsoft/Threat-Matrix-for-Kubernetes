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
|[MS-TA9024](../techniques/Connect%20from%20Proxy%20server.md)|Connect from Proxy Server|Limit network access from known proxy networks.|
|[MS-TA9030](../techniques/Access%20Kubelet%20API.md)|Access Kubelet API|Restrict access of pods to the Kubelet API using Network Policy, blocking pod traffic to the ports 10250 and 10255.|
|[MS-TA9031](../techniques/Network%20mapping.md)|Network Segmentation|Restrict network between pods using network policies|
|[MS-TA9032](../techniques/Access%20Kubernetes%20dasbhoard.md)|Access Kubernetes Dasbhoard|Restrict access to the Kubernetes dashboard service|
|[MS-TA9034](../techniques/Cluster%20internal%20networking.md)|Cluster Internal Networking|Provision pod network policies to restrict the traffic between pods|