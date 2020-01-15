# 2020-01-09

## Features

 - Helm charts:
   - gundeck: set soft limit to active max concurrent push metrics (#165)
   - backoffice: add missing backoffice second pod to offline download (#166)
   - nginz: sanitize access tokens from logs (#169)
   - brig: branding defaults to simplify customization (#168)
   - brig: added new config options (#173)
   - aws-ingress: added team settings and account pages (#42)
   - team-settings: updated to latest app (#175)
   - webapp: updated to latest app (#175)
   - account-pages: updated to latest app (#175)

## Other updates
- Standardise docs to use example.com everywhere (#161, #172)
- Cleaned up and moved docs around to wire-docs (#157)

## Breaking changes / known issues when upgrading

- None known

## Bug fixes
- Minor mc usage fix for minio


# 2019-09-30 #162

## Features

 - Helm charts:
   - Support for multiple helm repos (#151)
   - Default to using DaemonSet and externalTrafficPolicy as Local for the ingress (#121)
   - JSON logging for brig and galley, parser for nginz, making it friendly for kibana (#142)

 - Ansible:
   - Support multiple bucket bucket creation when provisioning minio (#153)
   - Host static files on minio to allow clients to point to custom backends (#155)

## Other updates
- Update script takes a path now (#140)
- Super simple k8s bootstrap (#150)

## Breaking changes / known issues when upgrading

- If using a kubernetes cluster installed with kubespray version kubespray master from 2018-10-09, i.e. commit 2ab2f3a0a3aeffdd9862bb485495b0c1e77a1ed8, the new DaemonSet default configuration will not work. See https://github.com/kubernetes-sigs/kubespray/issues/4036 for a detailed explanation and workaround.

## Bug fixes
- Fixed policy setting on minio for public files (#158)

## Internal Changes
- Lower default resource requirements (#152)