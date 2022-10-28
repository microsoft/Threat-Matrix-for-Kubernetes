---
hide:
  - toc
  - footer
---

# Restrict container runtime using LSM

!!! info inline end
    ID: MS-M9011<br>
    MITRE mitigation: [M1038](https://attack.mitre.org/mitigations/M1038/), [M1040](https://attack.mitre.org/mitigations/M1040/)


Restrict the running environment of the containers using Linux security modules, such as AppArmor, SELinux, Seccomp and others. Linux security modules can restrict access to files, running processes, certain system calls and others. Also, dropping unnecessary Linux capabilities from the container runtime environment helps reduce the attack surface of such container.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9006](../techniques/Exec%20into%20container.md)|Exec into container|Restrict container runtime capabilities using LSM.|
|[MS-TA9007](../techniques/bash%20or%20cmd%20inside%20container.md)|Bash or Cmd inside container|Restrict container runtime capabilities using LSM.|
|[MS-TA9009](../techniques/Application%20Exploit%20(RCE).md)|Application exploit (RCE)|Restrict container runtime capabilities using LSM.|
|[MS-TA9010](../techniques/SSH%20server%20running%20inside%20container.md)|SSH server running inside container|Limit which process can open network socket on a container.|
|[MS-TA9013](../techniques/Writable%20hostPath%20mount.md)|Writable hostPath mount|Use AppArmor to restrict file writing.|
|[MS-TA9039](../techniques/Resource%20hijacking.md)|Resource hijacking|Restrict execution of unwanted processes in containers.|
|[MS-TA9040](../techniques/Denial%20of%20service.md)|Denial of service|Restrict execution of unwanted processes in containers.|