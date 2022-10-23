---
hide:
  - toc
  - footer
---

# Malicious Admission Controller

!!! info inline end
    ID: MS-TA9015<br>
    Tactic: [Persistence](../tactics/Persistence/index.md), [Credential Access](../tactics/CredentialAccess/index.md) <br>
    MITRE technique: [T1546](https://attack.mitre.org/techniques/T1546/)

Admission controller is a Kubernetes component that intercepts, and possibly modifies, requests to the Kubernetes API server. There are two types of admissions controllers: validating and mutating controllers. As the name implies, a mutating admission controller can modify the intercepted request and change its properties. Kubernetes has a built-in generic admission controller named MutatingAdmissionWebhook. The behavior of this admission controller is determined by an admission webhook that the user deploys in the cluster. Attackers can use such webhooks for gaining persistence in the cluster. For example, attackers can intercept and modify the pod creation operations in the cluster and add their malicious container to every created pod.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9003](../mitigations/MS-M9003%20Adhere%20to%20least-privilege%20principle.md)|Adhere to least-privilege principle|Restrict permissions to deploy or modify `MutatingAdmissionWebhook` and `ValidatingAdmissionWebhook` objects.|