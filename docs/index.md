---
hide:
  - toc
  - footer
---

# Tactics

|[Initial Access](InitialAccess/index.md)|[Execution](Execution/index.md)|[Persistence](Persistence/index.md)|[Privilege Escalation](PrivilegeEscalation/index.md)|[Defense Evasion](DefenseEvasion/index.md)|[Credential Access](CredentialAccess/index.md)|[Discovery](Discovery/index.md)|[Lateral Movement](LateralMovement/index.md)|[Collection](Collection/index.md)|[Impact](Impact/index.md)|
|--------------|---------|-----------|--------------------|---------------|-----------------|---------|----------------|----------|------|
|Using Cloud Credentials|Exec into container|Backdoor container|Privileged container|Clear container logs|List K8S secrets|Access the K8S API server|Access cloud resources|images from a private registry|Data destruction|
|Compromised Image In Registry|bash/cmd inside container|Writable hostPath mount|Cluster-admin binding|Delete K8S events|Mount service principal|Access Kubelet API|Container service account||Resource hijacking|
|Kubeconfig file|New Container|Kubernetes CronJob|hostPath mount|Pod / container name similarily|Access container service account|Network mapping|Cluster internal networking||Denial of service|
|Application Vulnerability|Application Exploit (RCE)|Malicious admission controller|Access cloud resources|Connect from Proxy server|Application credentials in configuration files|Access Kubernetes dasbhoard|Application credentials in configuration files|||
|Exposed Dashboard|SSH server running inside container||||Access managed identity credentials|Instance Metadata API|Writable volume mount on host|||
|Exposed sensitive interfaces|Sidecar Injection||||Malicious Admission controller||Access Kubernetes dashboard|||
||||||||Access tiller endpoint|||
||||||||CoreDNS poisoning||
||||||||ARP poisoning and IP spoofing||



???+ attention "Disclaimer"
	The purpose of the Threat Matrix for Kubernetes is to educate readers on the potential of Kubernetes-based tactics, techniques, and procedures (TTPs). It is not to teach how to weaponize or specifically abuse them.
