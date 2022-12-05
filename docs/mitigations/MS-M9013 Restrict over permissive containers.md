---
hide:
  - toc
  - footer
---

# Restrict over permissive containers

!!! info inline end
    ID: MS-M9013<br>
    MITRE mitigation: [M1038](https://attack.mitre.org/mitigations/M1038/)


Use admission controller to prevent deploying containers with over-permissive capabilities or configuration in the cluster. This can include restricting privileged containers, containers with sensitive volumes, containers with excessive capabilities, and other signs of over permissive containers.

In AKS clusters which are configured to use service principal, the service principal credentials are stored in the `/etc/kubernetes/azure.json` file on the cluster nodes. Containers with access to a volume containing this file are considered as containers with sensitive mount.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9008](../techniques/New%20Container.md)|New container|Restrict over permissive containers in the cluster using admission controller.|
|[MS-TA9011](../techniques/Sidecar%20Injection.md)|Sidecar injection|Restrict over permissive containers in the cluster using admission controller.|
|[MS-TA9012](../techniques/Backdoor%20container.md)|Backdoor container|Restrict over permissive containers in the cluster using admission controller.|
|[MS-TA9013](../techniques/Writable%20hostPath%20mount.md)|Writable hostPath mount|Block sensitive volume mounts using admission controller.|
|[MS-TA9014](../techniques/Kubernetes%20CronJob.md)|Kubernetes CronJob|Check cronjob pod template for sensitive mounts and excessive permissions.|
|[MS-TA9018](../techniques/Privileged%20container.md)|Privileged container|Block Privileged containers using admission controller.|
|[MS-TA9020](../techniques/Access%20cloud%20resources.md)|Access cloud resources|Block mounting volumes with access to cloud credentials.|
|[MS-TA9026](../techniques/Mount%20service%20principal.md)|Mount service principal|Block sensitive volume mounts using admission controller|
|[MS-TA9036](../techniques/ARP%20poisoning%20and%20IP%20spoofing.md)|ARP poisoning and IP spoofing|Avoid NET_RAW capability in containers which would enable sending crafted packets that perform ARP poisoning.|
