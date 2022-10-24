---
hide:
  - toc
  - footer
---

# Privileged Container

!!! info inline end
    ID: MS-TA9018<br>
    Tactic: [Privilege Escalation](../tactics/PrivilegeEscalation/index.md) <br>
    MITRE technique: [T1610](https://attack.mitre.org/techniques/T1610/)

A privileged container is a container that has all the capabilities of the host machine, which lifts all the limitations regular containers have. Practically, this means that privileged containers can do almost every action that can be performed directly on the host. Attackers who gain access to a privileged container, or have permissions to create a new privileged container (by using the compromised pod’s service account, for example), can get access to the host’s resources.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9013](../mitigations/MS-M9013%20Limit%20Container%20Capabilities.md)|Limit Container Capabilities|Block privileged containers using admission controller.|
|[MS-M9017](../mitigations/MS-M9017%20Ensure%20that%20pods%20meet%20defined%20Pod%20Security%20Standards.md)|Ensure that pods meet defined Pod Security Standards|Restrict privileged containers using pod security standards.|
|[MS-M9005.003](../mitigations/MS-M9005/index.md)|Gate images deployed to Kubenertes cluster|Restrict deployment of new containers from trusted supply chain|