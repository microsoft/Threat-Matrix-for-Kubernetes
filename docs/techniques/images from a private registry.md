---
hide:
  - toc
  - footer
---

# Images from a private registry

!!! info inline end
    ID: MS-TA9037<br>
    Tactic: [Collection](../tactics/Collection/index.md) <br>
    MITRE technique: [T1530](https://attack.mitre.org/techniques/T1530/)

The images that are running in the cluster can be stored in a private registry. For pulling those images, the container runtime engine (such as Docker or containerd) needs to have valid credentials to those registries. If the registry is hosted by the cloud provider, in services like Azure Container Registry (ACR) or Amazon Elastic Container Registry (ECR), cloud credentials are used to authenticate to the registry. If attackers get access to the cluster, in some cases they can obtain access to the private registry and pull its images. For example, attackers can use the managed identity token as described in the “Access managed identity credential” technique. Similarly, in EKS, attackers can use the AmazonEC2ContainerRegistryReadOnly policy that is bound by default to the node’s IAM role.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9018](../mitigations/MS-M9018%20Restricting%20cloud%20metadata%20API%20access.md)|Restricting cloud metadata API access|Restrict access to IMDS to prevent authentication with a private registry using cloud identities.|
|[MS-M9003](../mitigations/MS-M9003%20Adhere%20to%20least-privilege%20principle.md)|Adhere to least-privilege principle|In some configurations, the credentials to private registries are stored as Kubernetes secret. Adhere to least-privilege principle to prevent users from reading image pull secrets.|