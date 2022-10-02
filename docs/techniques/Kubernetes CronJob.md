---
hide:
  - toc
  - footer
---

# Kubernetes CronJob

!!! info inline end
    ID: ???<br>
    Tactic: [Persistence](../tactics/Persistence/index.md) <br>
    MITRE technique: [T1053.007](https://attack.mitre.org/techniques/T1053/007/)

Kubernetes Job is a controller that creates one or more pods and ensures that a specified number of them successfully terminate. Kubernetes Job can be used to run containers that perform finite tasks for batch jobs. Kubernetes CronJob is used to schedule Jobs. Attackers may use Kubernetes CronJob for scheduling execution of malicious code that would run as a container in the cluster.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|