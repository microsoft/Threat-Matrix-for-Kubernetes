---
hide:
  - toc
  - footer
---

# Avoid using plain text credentials

!!! info inline end
    ID: MS-M9026<br>
    MITRE mitigation: -


Avoid using plain text credentials in configuration files. Use Kubernetes secrets or cloud secret store instead. This prevents unwanted access to plaintext credentials in source code, configuration files and Kubernetes objects.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9027](../techniques/Application%20credentials%20in%20configuration%20files.md)|Application credentials in configuration files|Avoid using plain text credentials in Kubernetes configuration|