---
hide:
  - toc
  - footer
---

# Tactics

|[Initial Access](tactics/InitialAccess/index.md)|[Execution](tactics/Execution/index.md)|[Persistence](tactics/Persistence/index.md)|[Privilege Escalation](tactics/PrivilegeEscalation/index.md)|[Defense Evasion](tactics/DefenseEvasion/index.md)|[Credential Access](tactics/CredentialAccess/index.md)|[Discovery](tactics/Discovery/index.md)|[Lateral Movement](tactics/LateralMovement/index.md)|[Collection](tactics/Collection/index.md)|[Impact](tactics/Impact/index.md)|
|--------------|---------|-----------|--------------------|---------------|-----------------|---------|----------------|----------|------|
|[Using Cloud Credentials](tactics/InitialAccess/Using%20Cloud%20Credentials.md)|[Exec into container](tactics/Execution/Exec%20into%20container.md)|[Backdoor container](tactics/Persistence/Backdoor%20container.md)|Privileged container|Clear container logs|List K8S secrets|Access the K8S API server|Access cloud resources|images from a private registry|Data destruction|
|[Compromised Image In Registry](tactics/InitialAccess/Compromised%20Image%20In%20Registry.md)|[bash/cmd inside container](tactics/Execution/bash%20or%20cmd%20inside%20container.md)|[Writable hostPath mount](tactics/Persistence/Writable%20hostPath%20mount.md)|Cluster-admin binding|Delete K8S events|Mount service principal|Access Kubelet API|Container service account||Resource hijacking|
|[Kubeconfig file](tactics/InitialAccess/Kubeconfig%20file.md)|[New Container](tactics/Execution/New%20Container.md)|[Kubernetes CronJob](tactics/Persistence/Kubernetes%20CronJob.md)|hostPath mount|Pod / container name similarily|Access container service account|Network mapping|Cluster internal networking||Denial of service|
|[Application Vulnerability](tactics/InitialAccess/Application%20Vulnerability.md)|[Application Exploit (RCE)](tactics/Execution/Application%20Exploit%20(RCE).md)|[Malicious admission controller](tactics/Persistence/Malicious%20admission%20controller.md)|Access cloud resources|Connect from Proxy server|Application credentials in configuration files|Access Kubernetes dasbhoard|Application credentials in configuration files|||
|[Exposed Dashboard](tactics/InitialAccess/Exposed%20Dashboard.md)|[SSH server running inside container](tactics/Execution/SSH%20server%20running%20inside%20container.md)||||Access managed identity credentials|Instance Metadata API|Writable volume mount on host|||
|[Exposed Sensitive Interfaces](tactics/InitialAccess/Exposed%20sensitive%20interfaces.md)|[Sidecar Injection](tactics/Execution/Sidecar%20Injection.md)||||Malicious Admission controller||Access Kubernetes dashboard|||
||||||||Access tiller endpoint|||
||||||||CoreDNS poisoning||
||||||||ARP poisoning and IP spoofing||



???+ attention "Disclaimer"
	The purpose of the Threat Matrix for Kubernetes is to educate readers on the potential of Kubernetes-based tactics, techniques, and procedures (TTPs). It is not to teach how to weaponize or specifically abuse them.
