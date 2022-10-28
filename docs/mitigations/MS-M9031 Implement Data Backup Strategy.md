---
hide:
  - toc
  - footer
---

# Implement data backup strategy

!!! info inline end
    ID: MS-M9031<br>
    MITRE mitigation: [M1053](https://attack.mitre.org/mitigations/M1053/)


Take and store data backups from pod mounted volumes for critical workloads. Ensure backup and storage systems are hardened and kept separate from the Kubernetes environment to prevent compromise.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9038](../techniques/Data%20destruction.md)|Data destruction|Backup pod mounted volumes for critical workloads.|
