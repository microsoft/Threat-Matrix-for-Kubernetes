---
hide:
  - toc
  - footer
---

# Bash or Cmd Inside Container

!!! info inline end
    ID: MS-TA9007 <br>
    Tactic: [Execution](../tactics/Execution/index.md) <br>
    MITRE technique: [T1059](https://attack.mitre.org/techniques/T1059/)



## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9011](../mitigations/MS-M9011%20Restrict%20Container%20Runtime%20using%20LSM.md)|Restrict Container Runtime using LSM|Restrict container runtime capabilities using LSM.|
|[MS-M9012](../mitigations/MS-M9012%20Remove%20Tools%20from%20Container%20Images.md)|Remove Tools from Container Images|Remove bash and other terminals from container images.|