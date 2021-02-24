# sseneca's k8s server

This repository contains all my server's deploy files.

## Architecture

This is for a bare-metal cluster, which for now only contains one node
that runs [Parabola GNU/Linux-libre](https://www.parabola.nu/).

Kubernetes is ran via [k3s](https://k3s.io).
[Flux](https://docs.fluxcd.io/en/1.21.2/) is used for GitOps as well as
automating e.g. image upgrades. I try to use Helm charts whenever I can
via the [Helm
Operator](https://docs.fluxcd.io/projects/helm-operator/en/stable/).
Secrets are [sealed](https://github.com/bitnami-labs/sealed-secrets).

## Caveats

- Flux and the Helm Operator need to be bootstrapped manually (via
  `fluxctl`)
- Node configuration isn't included
