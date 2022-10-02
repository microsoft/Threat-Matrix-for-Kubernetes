---
hide:
  - toc
  - footer
---

# Privileged Container

!!! info inline end
    ID: ???<br>
    Tactic: [Privilege Escalation](../PrivilegeEscalation/index.md) <br>
    MITRE technique: [T1610](https://attack.mitre.org/techniques/T1610/)

A privileged container is a container that has all the capabilities of the host machine, which lifts all the limitations regular containers have. Practically, this means that privileged containers can do almost every action that can be performed directly on the host. Attackers who gain access to a privileged container, or have permissions to create a new privileged container (by using the compromised pod’s service account, for example), can get access to the host’s resources.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|