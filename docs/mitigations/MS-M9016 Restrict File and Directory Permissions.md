---
hide:
  - toc
  - footer
---

# Restrict File and Directory Permissions

!!! info inline end
    ID: MS-M9016<br>
    MITRE mitigation: [M1022](https://attack.mitre.org/mitigations/M1022/)


When using `hostPath` volumes, set it to “read-only” mode if possible. This prevents the container from writing to files in the underlying node and will harden an escape from the container to the node.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9013](../techniques/Writable%20hostPath%20mount.md)|Writable hostPath Mount|Use read-only volumes.|
|[MS-TA9021](../techniques/Clear%20container%20logs.md)|Clear Container Logs|Restrict access to container logs.|