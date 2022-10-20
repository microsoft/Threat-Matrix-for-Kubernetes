---
hide:
  - toc
  - footer
---

# Exposed Sensitive Interfaces

!!! info inline end
    ID: MS-TA9005<br>
    Tactic: [Initial Access](../tactics/InitialAccess/index.md) <br>
    MITRE technique: [T1133](https://attack.mitre.org/techniques/T1133/)

Exposing a sensitive interface to the internet poses a security risk. Some popular frameworks were not intended to be exposed to the internet, and therefore don’t require authentication by default. Thus, exposing them to the internet allows unauthenticated access to a sensitive interface which might enable running code or deploying containers in the cluster by a malicious actor. Examples of such interfaces that were seen exploited include Apache NiFi, Kubeflow, Argo Workflows, Weave Scope, and the Kubernetes dashboard.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9008](../mitigations/MS-M9008%20Limit%20Access%20to%20Services%20Over%20Network.md)|Limit Access to Services Over Network|Limit access to sensitive interface over the Internet|
|[MS-M9009](../mitigations/MS-M9009%20Require%20Strong%20Authentication%20to%20Services.md)|Require Strong Authentication to Services|Require strong authentication to exposed services|