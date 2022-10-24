---
hide:
  - toc
  - footer
---

# Restrict access to the API server using IP firewall

!!! info inline end
    ID: MS-M9002<br>
    MITRE mitigation: [M1035](https://attack.mitre.org/mitigations/M1035/)

Restricting access to the API server can prevent unwanted access to the clusters management, even if the adversary achieved valid credentials to the cluster. 
In managed clusters, cloud providers often support native built-in firewall which can restrict the IP addresses that are allowed to access the API server.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9001](../techniques/Using%20Cloud%20Credentials.md)|Using Cloud Credentials|Restrict access of cloud accounts to API servers from known IP addresses|
|[MS-TA9003](../techniques/Kubeconfig%20file.md)|Kubeconfig file|Restrict access to the API server from known IP addresses|
|[MS-TA9024](../techniques/Connect%20from%20Proxy%20server.md)|Connect from Proxy Server|Restrict access to the API server from known IP addresses|