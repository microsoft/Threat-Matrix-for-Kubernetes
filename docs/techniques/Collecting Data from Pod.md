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


Using Kubernetes administrative commands an attacker can collect information from a pod without having to get direct access to that pod. One example of such a command is `kubectl cp` which can be used to copy files to and from pods. 

Another example is Kubelet Checpoint API which can be used to create a stateful copy of a running container. Typically a checkpoint contains all memory pages of all processes in the checkpointed container. This means that everything that used to be in memory is now available on the local disk. This includes all private data and possibly keys used for encryption.


## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9003](../mitigations/MS-M9003%20Adhere%20to%20least-privilege%20principle.md)|Adhere to least-privilege principle|Adhere to least-privilege principle to prevent users from checkpoint or running kubectl cp commands.|
|[MS-M9010](../mitigations/MS-M9010%20Restrict%20Exec%20Commands%20on%20Pods.md)|Restrict Exec Commands on Pods|Restrict checkpoint and other commands on pods using admissions controller.|