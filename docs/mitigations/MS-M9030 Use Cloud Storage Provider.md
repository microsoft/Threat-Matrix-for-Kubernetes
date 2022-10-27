---
hide:
  - toc
  - footer
---

# Use cloud storage provider

!!! info inline end
    ID: MS-M9030<br>
    MITRE mitigation: -


Use cloud storage services, such as Azure Files, for storing the application’s data. Kubernetes integrates with all main cloud provider storage services as storage providers for pod volumes. This allows leveraging cloud storage capabilities such as backup and snapshots.


## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----------|-----------|
|[MS-TA9038](../techniques/Data%20destruction.md)|Data destruction|Use Cloud Storage provider to persist application data.|
