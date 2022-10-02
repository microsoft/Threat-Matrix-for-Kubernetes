---
hide:
  - toc
  - footer
---

# Access Kubernetes API Server

!!! info inline end
    ID: ???<br>
    Tactic: [Discovery](../tactics/Discovery/index.md) <br>
    MITRE technique: [T1613](https://attack.mitre.org/techniques/T1613/)

The Kubernetes API server is the gateway to the cluster. Actions in the cluster are performed by sending various requests to the RESTful API. The status of the cluster, which includes all the components that are deployed on it, can be retrieved by the API server. Attackers may send API requests to probe the cluster and get information about containers, secrets, and other resources in the cluster.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|