---
hide:
  - toc
  - footer
---

# Exec Into Container

!!! info inline end
    ID: ???<br>
    Tactic: [Execution](../Execution/index.md) <br>
    MITRE technique: [T1609](https://attack.mitre.org/techniques/T1609/)

Attackers who have permissions, can run malicious commands in containers in the cluster using exec command (“kubectl exec”). In this method, attackers can use legitimate images, such as an OS image (e.g., Ubuntu) as a backdoor container, and run their malicious code remotely by using “kubectl exec”.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|