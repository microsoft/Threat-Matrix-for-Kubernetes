---
hide:
  - toc
  - footer
---

# Restrict file and directory permissions

!!! info inline end
    ID: MS-M9016<br>
    MITRE mitigation: [M1022](https://attack.mitre.org/mitigations/M1022/)


When using `hostPath` volumes, set it to “read-only” mode if possible. This prevents the container from writing to files in the underlying node and will harden an escape from the container to the node.

Kubelet monitors a specific folder on the node which contains static pods manifest. By default the location of static pod manifest on nodes is at `/etc/kubernetes/manifests`. Restrict access of users to this folder to avoid deployments of unwanted static pods.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9013](../techniques/Writable%20hostPath%20mount.md)|Writable hostPath mount|Use read-only volumes.|
|[MS-TA9021](../techniques/Clear%20container%20logs.md)|Clear container logs|Restrict access to container logs.|
|[MS-TA9017](../techniques/Static%20Pods.md)|Static pods|Restrict write access to the Static pods manifest folder.|