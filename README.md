# Vendor External DNS Global

Cluster-scoped [ExternalDNS](https://kubernetes-sigs.github.io/external-dns/) CRD
manifest for use in Kaptain deployments.

The DNSEndpoint CRD is extracted from the upstream ExternalDNS helm chart and
packaged separately so it can be installed once per cluster, independent of
namespace-scoped ExternalDNS instances.


## Contents

Single CRD manifest from the upstream helm chart's `crds/` directory, mapped to
the `src/kubernetes/` directory as `customresourcedefinition-dnsendpoints.yaml`.


## Versioning

Version tracks upstream ExternalDNS chart releases with an additional patch part
for packaging iterations. For example, `1.21.1.1` is the first packaging of
upstream chart `1.21.1`, `1.21.1.2` would be a packaging improvement without an
upstream change.

The upstream chart version is stored in `src/config/VendorHelmRenderedVersion`.


## Upstream

- Project: https://kubernetes-sigs.github.io/external-dns/
- Chart repo: `https://kubernetes-sigs.github.io/external-dns/`
- Chart name: `external-dns`
- CRDs sourced from: `crds/` in the rendered chart output
