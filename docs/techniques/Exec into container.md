---
hide:
  - toc
  - footer
---

# Exec into container

!!! info inline end
    ID: MS-TA9006<br>
    Tactic: [Execution](../tactics/Execution/index.md) <br>
    MITRE technique: [T1609](https://attack.mitre.org/techniques/T1609/)

Attackers who have permissions, can run malicious commands in containers in the cluster using exec command (“kubectl exec”). In this method, attackers can use legitimate images, such as an OS image (e.g., Ubuntu) as a backdoor container, and run their malicious code remotely by using “kubectl exec”.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9003](../mitigations/MS-M9003%20Adhere%20to%20least-privilege%20principle.md)|Adhere to least-privilege principle|Adhere to least-privilege principle to prevent users from exec into containers|
|[MS-M9010](../mitigations/MS-M9010%20Restrict%20Exec%20Commands%20on%20Pods.md)|Restrict Exec Commands on Pods|Restrict exec commands on pods using admissions controller.|
|[MS-M9011](../mitigations/MS-M9011%20Restrict%20Container%20Runtime%20using%20LSM.md)|Restrict Container Runtime using LSM|Restrict container runtime capabilities using LSM.|