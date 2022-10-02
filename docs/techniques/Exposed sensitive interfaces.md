---
hide:
  - toc
  - footer
---

# Exposed Sensitive Interfaces

!!! info inline end
    ID: ???<br>
    Tactic: [Initial Access](../tactics/InitialAccess/index.md) <br>
    MITRE technique: [T1133](https://attack.mitre.org/techniques/T1133/)

Exposing a sensitive interface to the internet poses a security risk. Some popular frameworks were not intended to be exposed to the internet, and therefore don’t require authentication by default. Thus, exposing them to the internet allows unauthenticated access to a sensitive interface which might enable running code or deploying containers in the cluster by a malicious actor. Examples of such interfaces that were seen exploited include Apache NiFi, Kubeflow, Argo Workflows, Weave Scope, and the Kubernetes dashboard.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|