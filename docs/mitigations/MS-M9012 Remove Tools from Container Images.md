---
hide:
  - toc
  - footer
---

# Remove tools from container images

!!! info inline end
    ID: MS-M9012<br>
    MITRE mitigation: [M1042](https://attack.mitre.org/mitigations/M1042/)


Attackers often use built-in executables to run their malicious code. Removing unused executables from the image filesystem can prevent such activity. Examples of executables that are commonly used in malicious activity include: sh, bash, curl, wget, chmod and more.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9007](../techniques/bash%20or%20cmd%20inside%20container.md)|Bash or Cmd inside container|Remove bash and other terminals from container images.|
|[MS-TA9039](../techniques/Resource%20hijacking.md)|Resource hijacking|Remove unused tools from the container image.|