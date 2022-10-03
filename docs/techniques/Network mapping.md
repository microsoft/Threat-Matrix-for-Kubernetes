---
hide:
  - toc
  - footer
---

# Network Mapping

!!! info inline end
    ID: MS-TA9031<br>
    Tactic: [Discovery](../tactics/Discovery/index.md) <br>
    MITRE technique: [T1046](https://attack.mitre.org/techniques/T1046/)

Attackers may try to map the cluster network to get information on the running applications, including scanning for known vulnerabilities. By default, there is no restriction on pods communication in Kubernetes. Therefore, attackers who gain access to a single container, may use it to probe the network.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|