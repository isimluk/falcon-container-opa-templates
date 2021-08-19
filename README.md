# falcon-container-opa-templates

This repository show-cases how to implement allow-listing of Falcon Container for OPA Gatekeeper based admission.

An example of OPA Gatekeeper based admission may be Anthos Config Manager (ACM). ACM provides [library of Kubernetes Hardening templates](https://cloud.google.com/anthos-config-management/docs/reference/constraint-template-library) that may be used as guidance for pod admission to the cluster.

If all the hardenings from Anthos library are applied to the cluster, Falcon Container product will not be able to operate as it needs certain permissions to be able to oversee the workloads.

To be able to allow-list certain permission for Falcon Container while keeping the otherworkloads constrained users are advised to modify stock templates from Anthos library. Proof-of-concept is available [in this repository](cluster/template-CustomK8sPSPCapabilities.yaml).

### Useful links
 * https://cloud.google.com/anthos-config-management/docs/concepts/policy-controller
 * https://github.com/GoogleCloudPlatform/acm-policy-controller-library
 * https://github.com/open-policy-agent/gatekeeper-library
 * https://github.com/open-policy-agent/gatekeeper-library/blob/master/library/pod-security-policy/capabilities/template.yaml
 * https://www.openpolicyagent.org/docs/latest/
 * https://play.openpolicyagent.org/p/axFzY0YI3X

