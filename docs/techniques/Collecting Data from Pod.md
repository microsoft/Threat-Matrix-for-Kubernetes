---
hide:
  - toc
  - footer
---

# Collecting Data from Pod

!!! info inline end
    ID: MS-TA9041<br>
    Tactic: [Collection](../tactics/Collection/index.md) <br>
    MITRE technique: 


Using Kubernetes administrative commands and attacker can collect information from a pod without having to get direct access to that pod. One example of such a command is `kubectl cp` which can be used to copy files to and from pods. 

Another example is Kubelet Checpoint API which can be used to create a stateful copy of a running container. Typically a checkpoint contains all memory pages of all processes in the checkpointed container. This means that everything that used to be in memory is now available on the local disk. This includes all private data and possibly keys used for encryption.


## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|