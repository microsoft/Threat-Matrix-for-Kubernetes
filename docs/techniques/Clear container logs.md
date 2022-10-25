---
hide:
  - toc
  - footer
---

# Clear Container Logs

!!! info inline end
    ID: MS-TA9021<br>
    Tactic: [Defense Evasion](../tactics/DefenseEvasion/index.md) <br>
    MITRE technique: [T1070](https://attack.mitre.org/techniques/T1070/)

Attackers may delete the application or OS logs on a compromised container in an attempt to prevent detection of their activity.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9020](../mitigations/MS-M9020%20Collect%20Logs%20to%20Remote%20Data%20Storage.md)|Collect Logs to Remote Data Storage|Collect container logs to a separate storage system.|
|[MS-M9016](../mitigations/MS-M9016%20Restrict%20File%20and%20Directory%20Permissions.md)|Restrict File and Directory Permissions|Restrict access to container logs.|