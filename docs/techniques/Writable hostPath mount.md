---
hide:
  - toc
  - footer
---

# Writable hostPath mount

!!! info inline end
    ID: MS-TA9013<br>
    Tactic: [Persistence](../tactics/Persistence/index.md), [Privilege Escalation](../tactics/PrivilegeEscalation/index.md), [Lateral Movement](../tactics/LateralMovement/index.md) <br>
    MITRE technique: [T1611](https://attack.mitre.org/techniques/T1611/)

hostPath volume mounts a directory or a file from the host to the container. Attackers who have permissions to create a new container in the cluster may create one with a writable hostPath volume and gain persistence on the underlying host. For example, the latter can be achieved by creating a cron job on the host.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9013](../mitigations/MS-M9013%20Restrict%20over%20permissive%20containers.md)|Restrict over permissive containers|Block sensitive volume mounts using admission controller.|
|[MS-M9016](../mitigations/MS-M9016%20Restrict%20File%20and%20Directory%20Permissions.md)|Restrict File and Directory Permissions|Use read-only volumes.|
|[MS-M9011](../mitigations/MS-M9011%20Restrict%20Container%20Runtime%20using%20LSM.md)|Restrict Container Runtime using LSM|Use AppArmor to restrict file writing.|
|[MS-M9017](../mitigations/MS-M9017%20Ensure%20that%20pods%20meet%20defined%20Pod%20Security%20Standards.md)|Ensure that pods meet defined Pod Security Standards|Use `Baseline` or `Restricted` pod security standards to prevent exploiting writable hostPath mount.|