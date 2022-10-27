---
hide:
  - toc
  - footer
---

# Connect from Proxy Server

!!! info inline end
    ID: MS-TA9024<br>
    Tactic: [Defense Evasion](../tactics/DefenseEvasion/index.md) <br>
    MITRE technique: [T1090](https://attack.mitre.org/techniques/T1090/)

Attackers may use proxy servers to hide their origin IP. Specifically, attackers often use anonymous networks such as TOR for their activity. This can be used for communicating with the applications themselves or with the API server.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9002](../mitigations/MS-M9002%20Restrict%20access%20to%20the%20API%20server%20using%20IP%20firewall.md)|Restrict access to the API server using IP firewall|Restrict access to the API server from known IP addresses|
|[MS-M9014](../mitigations/MS-M9014%20Network%20Segmentation.md)|Network Segmentation|Limit network access from known proxy networks.|
|[MS-M9021](../mitigations/MS-M9021%20Restrict%20the%20usage%20of%20unauthenticated%20APIs%20in%20the%20Cluster.md)|Restrict the usage of unauthenticated APIs in the cluster|Restrict unauthenticated API to the Kubernetes API server.|
|[MS-M9009](../mitigations/MS-M9009%20Require%20Strong%20Authentication%20to%20Services.md)|Require Strong Authentication to Services|Limit usage of kubeconfig authentication to the API server|
