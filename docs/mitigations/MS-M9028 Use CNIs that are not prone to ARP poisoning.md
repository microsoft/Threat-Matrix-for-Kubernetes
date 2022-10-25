---
hide:
  - toc
  - footer
---

# Use CNIs that are not prone to ARP poisoning

!!! info inline end
    ID: MS-M9028<br>
    MITRE mitigation: -


Kubernetes default CNI (Kubenet) is prone to ARP poisoning. This allows pods to impersonate other pods in the cluster.
Use alternative CNIs that are not prone to ARP poisoning in the cluster.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9036](../techniques/ARP%20poisoning%20and%20IP%20spoofing.md)|ARP poisoning and IP spoofing|Use CNIs that are not prone to ARP poisoning.|