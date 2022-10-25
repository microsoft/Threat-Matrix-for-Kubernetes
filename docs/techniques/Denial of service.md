---
hide:
  - toc
  - footer
---

# Denial of Service

!!! info inline end
    ID: MS-TA9040<br>
    Tactic: [Impact](../tactics/Impact/index.md) <br>
    MITRE technique: [T1498](https://attack.mitre.org/techniques/T1498/), [T1499](https://attack.mitre.org/techniques/T1499/)

Attackers may attempt to perform a denial of service attack, which makes the service unavailable to the legitimate users. In container clusters, this include attempts to block the availability of the containers themselves, the underlying nodes, or the API server.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9011](../mitigations/MS-M9011%20Restrict%20Container%20Runtime%20using%20LSM.md)|Restrict Container Runtime using LSM|Restrict execution of unwanted processes in containers.|
|[MS-M9002](../mitigations/MS-M9002%20Restrict%20access%20to%20the%20API%20server%20using%20IP%20firewall.md)|Restrict access to the API server using IP firewall|Restrict access to the API server from known IP addresses.|
|[MS-M9029](../mitigations/MS-M9029%20Set%20requests%20and%20limits%20for%20containers.md)|Set requests and limits for containers|Limit compute resources for containers.|