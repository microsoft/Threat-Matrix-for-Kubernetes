---
hide:
  - toc
  - footer
---

# Restrict Exec Commands on Pods

!!! info inline end
    ID: MS-M9010<br>
    MITRE mitigation: -


Restrict running Kubenetes `exec` command on sensitive\production containers using admission controller. This can prevent attackers from running malicious code on containers in cases when he `pods/exec` permission was obtained.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9006](../techniques/Exec%20into%20container.md)|Exec Into Container|Restrict exec commands on pods using admissions controller.|