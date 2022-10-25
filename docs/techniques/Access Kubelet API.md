---
hide:
  - toc
  - footer
---

# Access Kubelet API

!!! info inline end
    ID: MS-TA9030<br>
    Tactic: [Discovery](../tactics/Discovery/index.md) <br>
    MITRE technique: [T1613](https://attack.mitre.org/techniques/T1613/)

Kubelet is the Kubernetes agent that is installed on each node. Kubelet is responsible for the proper execution of pods that are assigned to the node. Kubelet exposes a read-only API service that does not require authentication (TCP port 10255). Attackers with network access to the host (for example, via running code on a compromised container) can send API requests to the Kubelet API. Specifically querying https://[NODE IP]:10255/pods/ retrieves the running pods on the node. https://[NODE IP]:10255/spec/ retrieves information about the node itself, such as CPU and memory consumption.

## Mitigations

|ID|Mitigation|Description|
|--|----------|-----------|
|[MS-M9009](../mitigations/MS-M9009%20Require%20Strong%20Authentication%20to%20Services.md)|Require Strong Authentication to Services|Avoid using the unsecured port 10255 for the Kubelet API|
|[MS-M9014](../mitigations/MS-M9014%20Network%20Segmentation.md)|Network Segmentation|Restrict access of pods to the Kubelet API using Network Policy, blocking pod traffic to the ports 10250 and 10255.|
|[MS-M9003](../mitigations/MS-M9003%20Adhere%20to%20least-privilege%20principle.md)|Adhere to least-privilege principle|Kubelet uses Kubernetes RBAC to authorize requests to its API, when `Webhook` is used as authorization mode. In this mode, Kubelet sends a `SubjectAccessReview` to the API server to check if the identity is authorized to perform the required action. Configure the Kubernetes RBAC such as only service accounts that should legitimacy communicate with Kubelet API have the relevant permissions.|
|[MS-M9027](../mitigations/MS-M9027%20Use%20NodeRestriction%20Admission%20Controller.md)|Use NodeRestriction Admission Controller|Limit Kubelet permissions to pods and nodes|