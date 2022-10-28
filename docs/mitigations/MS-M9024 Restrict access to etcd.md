---
hide:
  - toc
  - footer
---

# Restrict access to etcd

!!! info inline end
    ID: MS-M9024<br>
    MITRE mitigation: [M1035](https://attack.mitre.org/mitigations/M1035/)


Access to etcd should be limited to the Kubernetes control plane only. Depending on your configuration, you should attempt to use etcd over TLS. This mitigation is relevant only to non-managed Kubernetes environment, as access to etcd in cloud managed clusters is already restricted.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9025](../techniques/List%20K8S%20secrets.md)|List Kubernetes secrets|Restrict access to etcd.|