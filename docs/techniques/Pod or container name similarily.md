---
hide:
  - toc
  - footer
---

# Pod or Container Name Similarily

!!! info inline end
    ID: MS-TA9023<br>
    Tactic: [Defense Evasion](../tactics/DefenseEvasion/index.md) <br>
    MITRE technique: [T1036.005](https://attack.mitre.org/techniques/T1036/005/)

Pods that are created by controllers such as Deployment or DaemonSet have random suffix in their names. Attackers can use this fact and name their backdoor pods as they were created by the existing controllers. For example, an attacker could create a malicious pod named coredns-{random suffix} which would look related to the CoreDNS Deployment.

Also, attackers can deploy their containers in the kube-system namespace where the administrative containers reside.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9005.003](../mitigations/MS-M9005/MS-M9005.003%20Gate%20images%20deployed%20to%20Kubenertes%20cluster.md)|Gate images deployed to Kubenertes cluster|Restrict deployment of new containers from trusted supply chain|
