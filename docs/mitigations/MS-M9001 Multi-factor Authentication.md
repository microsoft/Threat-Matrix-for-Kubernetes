---
hide:
  - toc
  - footer
---

# Multi-factor Authentication

!!! info inline end
    ID: MS-M9001<br>
    MITRE mitigation: [M1032](https://attack.mitre.org/mitigations/M1032/)

Using multi-factor authentication for accounts can prevent unauthorized access in case an adversary achieves access to the account credentials. This can reduce the risk in case an adversary achieved valid credentials to an account that has permissions to the Kubernetes cluster.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9001](../techniques/Using%20Cloud%20Credentials.md)|Using Cloud Credentials|Use multi-factor authentication for cloud accounts which can be elevated to access Kubernetes clusters in that cloud.|