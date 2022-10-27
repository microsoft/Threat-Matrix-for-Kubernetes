---
hide:
  - toc
  - footer
---

# Disable service account auto mount

!!! info inline end
    ID: MS-M9025<br>
    MITRE mitigation: -


By default, a service account is mounted to every pod. If the application doesn’t require access to the Kubernetes API, disable the service account auto-mount by specifying `automountServiceAccountToken: false` in the pod configuration.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9016](../techniques/container%20service%20account.md)|Container service account|Disable service account auto mount.|