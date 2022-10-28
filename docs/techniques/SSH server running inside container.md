---
hide:
  - toc
  - footer
---

# SSH server running inside container

!!! info inline end
    ID: MS-TA9010<br>
    Tactic: [Execution](../tactics/Execution/index.md) <br>
    MITRE technique: 

SSH server that is running inside a container may be used by attackers. If attackers gain valid credentials to a container, whether by brute force attempts or by other methods (such as phishing), they can use it to get remote access to the container by SSH.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9015](../mitigations/MS-M9015%20Avoid%20Running%20Management%20Interface%20on%20Containers.md)|Avoid Running Management Interface on Containers|Avoid running SSH daemon on containers|
|[MS-M9014](../mitigations/MS-M9014%20Network%20Segmentation.md)|Network Segmentation|Limit network access to containers|
|[MS-M9011](../mitigations/MS-M9011%20Restrict%20Container%20Runtime%20using%20LSM.md)|Restrict Container Runtime using LSM|Limit which process can open network socket on a container.|