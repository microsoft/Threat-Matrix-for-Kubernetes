---
hide:
  - toc
  - footer
---

# Resource hijacking

!!! info inline end
    ID: MS-TA9039<br>
    Tactic: [Impact](../tactics/Impact/index.md) <br>
    MITRE technique: [T1496](https://attack.mitre.org/techniques/T1496/)

Attackers may abuse a compromised resource for running tasks. A common abuse is to use compromised resources for running digital currency mining. Attackers who have access to a container in the cluster or have permissions to create new containers may use them for such activity.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9011](../mitigations/MS-M9011%20Restrict%20Container%20Runtime%20using%20LSM.md)|Restrict Container Runtime using LSM|Restrict execution of unwanted processes in containers.|
|[MS-M9012](../mitigations/MS-M9012%20Remove%20Tools%20from%20Container%20Images.md)|Remove Tools from Container Images|Remove unused tools from the container image.|