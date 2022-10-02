---
hide:
  - toc
  - footer
---

# Backdoor Container

!!! info inline end
    ID: ???<br>
    Tactic: [Persistence](../Persistence/index.md) <br>
    MITRE technique: [T1569](https://attack.mitre.org/techniques/T1569/)

Attackers run their malicious code in a container in the cluster. By using the Kubernetes controllers such as DaemonSets or Deployments, attackers can ensure that a constant number of containers run in one, or all, the nodes in the cluster.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|