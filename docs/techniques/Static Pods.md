---
hide:
  - toc
  - footer
---

# Static Pods

!!! info inline end
    ID: MS-TA9017<br>
    Tactic: [Persistence](../tactics/Persistence/index.md) <br>
    MITRE technique: 

Static Pods are created and managed by the the kubelete daemon on each node, without the API server observing them. Kubelet watches each static pod and restart it if it fails.  

Kubelet automatically tries to create a mirror pod on the Kubernetes API server to represent the static pods, so it will be visibile on the API server, however the pods cannot be controlled from there.

Static Pods are created based on a web or local filesystem YAML files which kubelet observes for changes.
An attacker can use the static pods manifest file to ensure that a pod is always running on a cluster node and prevent it from being changed or deleted from the Kubernetes API server.


## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9016](../mitigations/MS-M9016%20Restrict%20File%20and%20Directory%20Permissions.md)|Restrict File and Directory Permissions|Restrict write access to the static pods manifest folder.|
|[MS-M9032](../mitigations/MS-M9032%20Avoid%20using%20web-hosted%20manifest%20for%20Kubelet.md)|Avoid using web-hosted manifest for Kubelet|Avoid using web-hosted manifest for Kubelet.|