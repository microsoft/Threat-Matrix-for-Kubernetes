---
hide:
  - toc
  - footer
---

# Data Destruction

!!! info inline end
    ID: MS-TA9038<br>
    Tactic: [Impact](../tactics/Impact/index.md) <br>
    MITRE technique: [T1485](https://attack.mitre.org/techniques/T1485/)

Attackers may attempt to destroy data and resources in the cluster. This includes deleting deployments, configurations, storage, and compute resources.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9030](../mitigations/MS-M9030%20Use%20Cloud%20Storage%20Provider.md)|Use Cloud Storage Provider|Use Cloud Storage provider to persist application data.|
|[MS-M9031](../mitigations/MS-M9031%20Implement%20Data%20Backup%20Strategy.md)|Implement Data Backup Strategy|Backup pod mounted volumes for critial workloads.|