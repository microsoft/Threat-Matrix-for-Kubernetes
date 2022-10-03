---
hide:
  - toc
  - footer
---

# Static Pods

!!! info inline end
    ID: ???<br>
    Tactic: [Persistence](../tactics/Persistence/index.md) <br>
    MITRE technique: 

Static Pods are created and managed by the the kubelete daemon on each node, without the API server observing them. Kubelet watches each static pod and restart it if it fails.  

Kubelet automatically tries to create a mirror pod on the Kubernetes API server to represent the static pods, so it will be visibile on the API server, however the pods cannot be controlled from there.

Static Pods are created based on a web or local filesystem YAML files which kubelet observes for changes.
An attacker can use the static pods manifest file to ensure that a pod is always running on a cluster node and prevent it from being changed or deleted from the Kubernetes API server.


## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|