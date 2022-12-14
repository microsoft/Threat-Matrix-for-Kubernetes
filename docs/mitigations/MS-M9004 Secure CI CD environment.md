---
hide:
  - toc
  - footer
---

# Secure CI/CD environment

!!! info inline end
    ID: MS-M9004<br>
    MITRE mitigation: -


Security code repositories and CI/CD environment by placing gates to restrict unauthorized access and modification of content. This can include enforcing RBAC permissions to access and make changes to code, artifacts and build pipelines, ensure governed process for pull-request approval, apply branch policies and others.



## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9002](../techniques/Compromised%20Image%20In%20Registry.md)|Compromised image in registry|Placing gates in the CI\CD process can block pushing unsecured code to the image registry.|
