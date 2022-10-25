---
hide:
  - toc
  - footer
---

# Limit Access to Services Over Network

!!! info inline end
    ID: MS-M9008<br>
    MITRE mitigation: [M1035](https://attack.mitre.org/mitigations/M1035/)


Avoid exposing sensitive interfaces insecurely to the Internet or limit access to it. Sensitive interfaces includes management tools and applications that allow creation of new containers in the cluster. Some of those services does not use authentication by default and are not intended to be exposed. Examples of services that were exploited: Weave Scope, Apache NiFi and more.

If services need to be exposed to the internet and are exposed using `LoadBalancer` service, use IP restriction (`loadBalancerSourceRanges`) when possible. This reduces the attack surface of the application and can prevent attackers from being able to reach the sensitive interfaces.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9005](../techniques/Exposed%20sensitive%20interfaces.md)|Exposed Sensitive Interfaces|Limit access to sensitive interface over the Internet|
|[MS-TA9032](../techniques/Access%20Kubernetes%20dasbhoard.md)|Access Kubernetes Dasbhoard|Restrict access to the Kubernetes dashboard service|
