---
hide:
  - toc
  - footer
---

# Writable hostPath Mount

!!! info inline end
    ID: MS-TA9013<br>
    Tactic: [Persistence](../tactics/Persistence/index.md), [Privilege Escalation](../tactics/PrivilegeEscalation/index.md), [Lateral Movement](../tactics/LateralMovement/index.md) <br>
    MITRE technique: [T1611](https://attack.mitre.org/techniques/T1611/)

hostPath volume mounts a directory or a file from the host to the container. Attackers who have permissions to create a new container in the cluster may create one with a writable hostPath volume and gain persistence on the underlying host. For example, the latter can be achieved by creating a cron job on the host.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|