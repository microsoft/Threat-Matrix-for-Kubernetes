---
hide:
  - toc
  - footer
---

# Avoid running management interface on containers

!!! info inline end
    ID: MS-M9015<br>
    MITRE mitigation: [M1042](https://attack.mitre.org/mitigations/M1042/)


Avoid running SSH daemon, as well as other management interfaces, if they aren’t necessary for the application’s functionality.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9010](../techniques/SSH%20server%20running%20inside%20container.md)|SSH server running inside container|Avoid running SSH daemon on containers|