---
hide:
  - toc
  - footer
---

# Restricting cloud metadata API access

!!! info inline end
    ID: MS-M9018<br>
    MITRE mitigation: [M1035](https://attack.mitre.org/mitigations/M1035/)


Many cluster-to-cloud authentication methods involve access to the node’s metadata server. Restrict access to the metadata server if it’s not necessary. This can be done at the pod level by using networking restriction tools such as network policies. Alternatively, cloud providers allow this functionality in the node\cluster level. For instance, in AWS one can restrict the hop count limit of IMDS as described [here](https://aws.github.io/aws-eks-best-practices/security/docs/iam/#restrict-access-to-the-instance-profile-assigned-to-the-worker-node). In AKS, deploying `AAD pod identity` would restrict access to IMDS.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9020](../techniques/Access%20cloud%20resources.md)|Access cloud resources|Restrict the access of pods to IMDS to restrict pods from getting access to cloud identities.|
|[MS-TA9028](../techniques/Access%20managed%20identity%20credentials.md)|Access Managed Identity Credentials|Restrict the access of pods to IMDS|
|[MS-TA9033](../techniques/Instance%20Metadata%20API.md)|Instance Metadata API|Restrict the access of pods to IMDS|