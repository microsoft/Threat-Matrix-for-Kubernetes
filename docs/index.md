---
hide:
  - toc
  - footer
---

# Tactics

|[Initial Access](tactics/InitialAccess/index.md)|[Execution](tactics/Execution/index.md)|[Persistence](tactics/Persistence/index.md)|[Privilege Escalation](tactics/PrivilegeEscalation/index.md)|[Defense Evasion](tactics/DefenseEvasion/index.md)|[Credential Access](tactics/CredentialAccess/index.md)|[Discovery](tactics/Discovery/index.md)|[Lateral Movement](tactics/LateralMovement/index.md)|[Collection](tactics/Collection/index.md)|[Impact](tactics/Impact/index.md)|
|--------------|---------|-----------|--------------------|---------------|-----------------|---------|----------------|----------|------|
|[Using Cloud Credentials](tactics/InitialAccess/Using%20Cloud%20Credentials.md)|[Exec into container](tactics/Execution/Exec%20into%20container.md)|[Backdoor container](tactics/Persistence/Backdoor%20container.md)|[Privileged container](tactics/PrivilegeEscalation/Privileged%20container.md)|[Clear container logs](tactics/DefenseEvasion/Clear%20container%20logs.md)|[List K8S secrets](tactics/CredentialAccess/List%20K8S%20secrets.md)|[Access the K8S API server](tactics/Discovery/Access%20the%20K8S%20API%20server.md)|Access cloud resources|images from a private registry|Data destruction|
|[Compromised Image In Registry](tactics/InitialAccess/Compromised%20Image%20In%20Registry.md)|[bash/cmd inside container](tactics/Execution/bash%20or%20cmd%20inside%20container.md)|[Writable hostPath mount](tactics/Persistence/Writable%20hostPath%20mount.md)|[Cluster-admin binding](tactics/PrivilegeEscalation/Cluster-admin%20binding.md)|[Delete K8S events](tactics/DefenseEvasion/Delete%20K8S%20events.md)|[Mount service principal](tactics/CredentialAccess/Mount%20service%20principal.md)|[Access Kubelet API](tactics/Discovery/Access%20Kubelet%20API.md)|Container service account||Resource hijacking|
|[Kubeconfig file](tactics/InitialAccess/Kubeconfig%20file.md)|[New Container](tactics/Execution/New%20Container.md)|[Kubernetes CronJob](tactics/Persistence/Kubernetes%20CronJob.md)|[hostPath mount](tactics/Persistence/Writable%20hostPath%20mount.md)|[Pod / container name similarily](tactics/DefenseEvasion/Pod%20or%20container%20name%20similarily.md)|[Access container service account](tactics/CredentialAccess/Access%20container%20service%20account.md)|[Network mapping](tactics/Discovery/Network%20mapping.md)|Cluster internal networking||Denial of service|
|[Application Vulnerability](tactics/InitialAccess/Application%20Vulnerability.md)|[Application Exploit (RCE)](tactics/Execution/Application%20Exploit%20(RCE).md)|[Malicious admission controller](tactics/Persistence/Malicious%20admission%20controller.md)|[Access cloud resources](tactics/PrivilegeEscalation/Access%20cloud%20resources.md)|[Connect from Proxy server](tactics/DefenseEvasion/Connect%20from%20Proxy%20server.md)|[Application credentials in configuration files](tactics/CredentialAccess/Application%20credentials%20in%20configuration%20files.md)|[Access Kubernetes dasbhoard](tactics/Discovery/Access%20Kubernetes%20dasbhoard.md)|Application credentials in configuration files|||
|[Exposed Dashboard](tactics/InitialAccess/Exposed%20Dashboard.md)|[SSH server running inside container](tactics/Execution/SSH%20server%20running%20inside%20container.md)||||[Access managed identity credentials](tactics/CredentialAccess/Access%20managed%20identity%20credentials.md)|[Instance Metadata API](tactics/Discovery/Instance%20Metadata%20API.md)|Writable volume mount on host|||
|[Exposed Sensitive Interfaces](tactics/InitialAccess/Exposed%20sensitive%20interfaces.md)|[Sidecar Injection](tactics/Execution/Sidecar%20Injection.md)||||[Malicious Admission controller](tactics/Persistence/Malicious%20admission%20controller.md)||Access Kubernetes dashboard|||
||||||||Access tiller endpoint|||
||||||||CoreDNS poisoning||
||||||||ARP poisoning and IP spoofing||



???+ attention "Disclaimer"
	The purpose of the Threat Matrix for Kubernetes is to educate readers on the potential of Kubernetes-based tactics, techniques, and procedures (TTPs). It is not to teach how to weaponize or specifically abuse them.
