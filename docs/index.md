---
hide:
  - toc
  - footer
---

# Tactics

|[Initial Access](tactics/InitialAccess/index.md)|[Execution](tactics/Execution/index.md)|[Persistence](tactics/Persistence/index.md)|[Privilege Escalation](tactics/PrivilegeEscalation/index.md)|[Defense Evasion](tactics/DefenseEvasion/index.md)|[Credential Access](tactics/CredentialAccess/index.md)|[Discovery](tactics/Discovery/index.md)|[Lateral Movement](tactics/LateralMovement/index.md)|[Collection](tactics/Collection/index.md)|[Impact](tactics/Impact/index.md)|
|--------------|---------|-----------|--------------------|---------------|-----------------|---------|----------------|----------|------|
|[Using Cloud Credentials](tactics/InitialAccess/Using%20Cloud%20Credentials.md)|Exec into container|Backdoor container|Privileged container|Clear container logs|List K8S secrets|Access the K8S API server|Access cloud resources|images from a private registry|Data destruction|
|[Compromised Image In Registry](tactics/InitialAccess/Compromised%20Image%20In%20Registry.md)|bash/cmd inside container|Writable hostPath mount|Cluster-admin binding|Delete K8S events|Mount service principal|Access Kubelet API|Container service account||Resource hijacking|
|[Kubeconfig file](tactics/InitialAccess/Kubeconfig%20file.md)|New Container|Kubernetes CronJob|hostPath mount|Pod / container name similarily|Access container service account|Network mapping|Cluster internal networking||Denial of service|
|[Application Vulnerability](tactics/InitialAccess/Application%20Vulnerability.md)|Application Exploit (RCE)|Malicious admission controller|Access cloud resources|Connect from Proxy server|Application credentials in configuration files|Access Kubernetes dasbhoard|Application credentials in configuration files|||
|[Exposed Dashboard](tactics/InitialAccess/Exposed%20Dashboard.md)|SSH server running inside container||||Access managed identity credentials|Instance Metadata API|Writable volume mount on host|||
|[Exposed Sensitive Interfaces](tactics/InitialAccess/Exposed%20sensitive%20interfaces.md)|Sidecar Injection||||Malicious Admission controller||Access Kubernetes dashboard|||
||||||||Access tiller endpoint|||
||||||||CoreDNS poisoning||
||||||||ARP poisoning and IP spoofing||



???+ attention "Disclaimer"
	The purpose of the Threat Matrix for Kubernetes is to educate readers on the potential of Kubernetes-based tactics, techniques, and procedures (TTPs). It is not to teach how to weaponize or specifically abuse them.
