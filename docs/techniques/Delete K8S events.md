---
hide:
  - toc
  - footer
---

# Delete Kubernetes Events

!!! info inline end
    ID: MS-TA9022<br>
    Tactic: [Defense Evasion](../tactics/DefenseEvasion/index.md) <br>
    MITRE technique: [T1070](https://attack.mitre.org/techniques/T1070/)

A Kubernetes event is a Kubernetes object that logs state changes and failures of the resources in the cluster. Example events are a container creation, an image pull, or a pod scheduling on a node.

Kubernetes events can be very useful for identifying changes that occur in the cluster. Therefore, attackers may want to delete these events (e.g., by using: “kubectl delete events–all”) in an attempt to avoid detection of their activity in the cluster.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9020](../mitigations/MS-M9020%20Collect%20Logs%20to%20Remote%20Data%20Storage.md)|Collect Logs to Remote Data Storage|Collect Kubernetes logs to a separate storage system.|
|[MS-M9003](../mitigations/MS-M9003%20Adhere%20to%20least-privilege%20principle.md)|Adhere to least-privilege principle|Restrict permissions to delete Kubernetes events.|