---
hide:
  - toc
  - footer
---

# Compromised image In registry

!!! info inline end
    ID: MS-TA9002<br>
    Tactic: [Initial Access](../tactics/InitialAccess/index.md) <br>
    MITRE technique: [T1195.002](https://attack.mitre.org/techniques/T1195/002/), [T1525](https://attack.mitre.org/techniques/T1525/)

Running a compromised image in a cluster can compromise the cluster. Attackers who get access to a private registry can plant their own compromised images in the registry. The latter can then be pulled by a user. In addition, users often use untrusted images from public registries (such as Docker Hub) that may be malicious.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9004](../mitigations/MS-M9004%20Secure%20CI%20CD%20environment.md)|Secure CI/CD environment|Placing gates in the CI\CD process can block pushing unsecured code to container images.|
|[MS-M9005](../mitigations/MS-M9005/index.md)|Image Assurance Policy|Ensure that only images that passed the security compliance policies are pushed to registries and deployed to Kubernetes clusters.|