---
hide:
  - toc
  - footer
---

# Limit Container Capabilities

!!! info inline end
    ID: MS-M9013<br>
    MITRE mitigation: [M1038](https://attack.mitre.org/mitigations/M1038/)


Use admission controller to prevent deploying containers with over-permissive capabilities in the cluster. This can include restricting privilege containers, containers with sensitive volumes, containers with excessive capabilities, and other signs of over permissive containers.

In AKS clusters which are configured to use service principal, holds the credentials to such service principal in the `/etc/kubernetes/azure.json` file on the cluster nodes. Containers with access to a volume containing this file are considered as containers with sensitive mount.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9008](../techniques/New%20Container.md)|New Container|Restrict over permissive containers in the cluster using admission controller.|
|[MS-TA9011](../techniques/Sidecar%20Injection.md)|Sidecar Injection|Restrict over permissive containers in the cluster using admission controller.|
|[MS-TA9012](../techniques/Backdoor%20container.md)|Backdoor Container|Restrict over permissive containers in the cluster using admission controller.|
|[MS-TA9013](../techniques/Writable%20hostPath%20mount.md)|Writable hostPath Mount|Block sensitive volume mounts using admission controller.|
|[MS-TA9014](../techniques/Kubernetes%20CronJob.md)|Kubernetes CronJob|Check cronjob pod template for sensitive mounts and excessive permissions.|
|[MS-TA9018](../techniques/Privileged%20container.md)|Privileged Container|Block privileged containers using admission controller.|
|[MS-TA9020](../techniques/Access%20cloud%20resources.md)|Access cloud resources|Block mounting volumes with access to cloud credentials.|
|[MS-TA9026](../techniques/Mount%20service%20principal.md)|Mount Service Principal|Block sensitive volume mounts using admission controller|
