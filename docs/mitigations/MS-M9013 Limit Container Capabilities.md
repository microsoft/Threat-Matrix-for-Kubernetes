---
hide:
  - toc
  - footer
---

# Limit Container Capabilities

!!! info inline end
    ID: MS-M9013<br>
    MITRE mitigation: -


Use admission controller to prevent deploying containers with over-permissive capabilities in the cluster. This can include restricting privilege containers, containers with sensitive volumes, containers with excessive capabilities, and other signs of over permissive containers.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9008](../techniques/New%20Container.md)|New Container|Restrict over permissive containers in the cluster using admission controller.|
|[MS-TA9011](../techniques/Sidecar%20Injection.md)|Sidecar Injection|Restrict over permissive containers in the cluster using admission controller.|
|[MS-TA9012](../techniques/Backdoor%20container.md)|Backdoor Container|Restrict over permissive containers in the cluster using admission controller.|
|[MS-TA9013](../techniques/Writable%20hostPath%20mount.md)|Writable hostPath Mount|Block sensitive volume mounts using admission controller.|