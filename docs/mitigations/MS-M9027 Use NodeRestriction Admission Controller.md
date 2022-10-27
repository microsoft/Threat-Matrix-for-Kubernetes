---
hide:
  - toc
  - footer
---

# Use NodeRestriction admission controller

!!! info inline end
    ID: MS-M9027<br>
    MITRE mitigation: -


NodeRestriction admission controller limits the permissions of kubelet and allows it to modify only its own Node object and only the pods that are running on its own node. This may limit attackers who have access to the Kubelet API from gaining full control over the cluster.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9030](../techniques/Access%20Kubelet%20API.md)|Access Kubelet API|Limit Kubelet permissions to pods and nodes|