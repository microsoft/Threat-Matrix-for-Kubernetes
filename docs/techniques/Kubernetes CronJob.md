---
hide:
  - toc
  - footer
---

# Kubernetes CronJob

!!! info inline end
    ID: MS-TA9014<br>
    Tactic: [Persistence](../tactics/Persistence/index.md) <br>
    MITRE technique: [T1053.007](https://attack.mitre.org/techniques/T1053/007/)

Kubernetes Job is a controller that creates one or more pods and ensures that a specified number of them successfully terminate. Kubernetes Job can be used to run containers that perform finite tasks for batch jobs. Kubernetes CronJob is used to schedule Jobs. Attackers may use Kubernetes CronJob for scheduling execution of malicious code that would run as a container in the cluster.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9005.003](../mitigations/MS-M9005/index.md)|Gate images deployed to Kubernetes cluster|Restrict deployment of new containers from trusted supply chain|
|[MS-M9003](../mitigations/MS-M9003%20Adhere%20to%20least-privilege%20principle.md)|Adhere to least-privilege principle|Prevent unnecessary users and service accounts from creating new cronjobs.|
|[MS-M9013](../mitigations/MS-M9013%20Restrict%20over%20permissive%20containers.md)|Restrict over permissive containers|Check cronjob pod template for sensitive mounts and excessive permissions.|