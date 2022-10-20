---
hide:
  - toc
  - footer
---

# Image Assurance Policy

!!! info inline end
    ID: MS-M9005<br>
    MITRE mitigation: [M1016](https://attack.mitre.org/mitigations/M1016/), [M1045](https://attack.mitre.org/mitigations/M1045/)


Apply image assurance policy to evaluate container images against vulnerabilities, malwares, exposed secrets or other policies. By ensuring consistent and comperhensive image assurance policy across the build, ship and run development stages.

One approach of ensuring images passes assurance or compliance checks it to sign the container images, so the image signature can be checks downstream when deploying to Kubernetes clusters at runtime.


!!! abstract "Sub-mitigations"

    |ID|Name|
    |--|----|
    |[MS-M9005.001](./MS-M9005.001%20Gate%20generated%20images%20in%20CI%20CD%20pipeline.md)|[Gate generated images in CI/CD pipeline](./MS-M9005.001%20Gate%20generated%20images%20in%20CI%20CD%20pipeline.md)|
    |[MS-M9005.002](./MS-M9005.002%20Gate%20images%20pushed%20to%20registries.md)|[Gate images pushed to registries](./MS-M9005.002%20Gate%20images%20pushed%20to%20registries.md)|
    |[MS-M9005.003](./MS-M9005.003%20Gate%20images%20deployed%20to%20Kubenertes%20cluster.md)|[Gate images deployed to Kubenertes cluster](./MS-M9005.003%20Gate%20images%20deployed%20to%20Kubenertes%20cluster.md)|




## Techniques Addressed by Mitigation

|ID|Name|Use|
|--|----|---|
|[MS-TA9002](../../techniques/Compromised%20Image%20In%20Registry.md)|Compromised Image In Registry|Ensure that only images that passed the security compliance policies are pushed to registries and deployed to Kubenetes clusters.|
|[MS-TA9004](../../techniques/Application%20Vulnerability.md)|Application Vulnerability|Scan images for vulnerabilities|
