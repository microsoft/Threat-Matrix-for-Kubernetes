---
hide:
  - toc
  - footer
---

# Restrict exec commands on pods

!!! info inline end
    ID: MS-M9010<br>
    MITRE mitigation: -


Restrict running Kubenetes `exec` command on sensitive\production containers using admission controller. This can prevent attackers from running malicious code on containers in cases when he `pods/exec` permission was obtained.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9006](../techniques/Exec%20into%20container.md)|Exec into container|Restrict exec commands on pods using admissions controller.|
|[MS-TA9041](../techniques/Collecting%20Data%20from%20Pod.md)|Collecting data from pod|Restrict checkpoint and other commands on pods using admissions controller.|