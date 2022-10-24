---
hide:
  - toc
  - footer
---

# Application Credentials in Configuration Files

!!! info inline end
    ID: MS-TA9027<br>
    Tactic: [Credential Access](../tactics/CredentialAccess/index.md), [Lateral Movement](../tactics/LateralMovement/index.md) <br>
    MITRE technique: [T1552](https://attack.mitre.org/techniques/T1552/)

Developers store secrets in the Kubernetes configuration files, such as environment variables in the pod configuration. Such behavior is commonly seen in clusters that are monitored by Microsoft Defender for Cloud. Attackers who have access to those configurations, by querying the API server or by accessing those files on the developer’s endpoint, can steal the stored secrets and use them.

Using those credentials attackers may gain access to additional resources inside and outside the cluster. 

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9026](../mitigations/MS-M9026%20Avoid%20using%20plain%20text%20credentials%20in%20configuration%20files.md)|Avoid using plain text credentials|Avoid using plain text credentials in Kubernetes configuration|
|[MS-M9022](../mitigations/MS-M9022%20Use%20Managed%20Secret%20Store.md)|Use Managed Secret Store|Store secrets securely in managed secret stores|