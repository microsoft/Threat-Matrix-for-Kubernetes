---
hide:
  - toc
  - footer
---

# Network Intrusion Prevention

!!! info inline end
    ID: MS-M9007<br>
    MITRE mitigation: [M1031](https://attack.mitre.org/mitigations/M1031/)


Use intrusion detection signatures and web application firewall to block traffic at network boundaries to pods and services in a Kubernetes cluster.

Adapting the network intrusion prevention solution to Kubernetes environment might be needed to route network traffic destined to services through it. 
In some cases, this will be done by deploying a containarized version of a network intrusion prevention solution to the Kubernetes cluster and be part of the cluster network, and in some cases, routing ingress traffic to Kubernetes services through an external appliance, requiring that all ingress traffic will only come from such an appliance.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9004](../techniques/Application%20Vulnerability.md)|Application Vulnerability|Use network intrusion prevenetion to block exploiting vulnerabilities.|