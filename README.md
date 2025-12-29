# Homelab Documentation

This git repository acts as overview of my Homelab configuration.
Due to different technology stacks, the configuration is split into multiple git repositories.

**Note:** All repositories on GitHub are only a mirror. The main work is done on my self-hosted GitLab instance, which has two self-hosted GitLab runners attached and Renovate configured.

## Repositories

- [homelab-terraform](https://github.com/QuantumDancer/homelab-terraform): Terraform configuration to create new VMs on my Proxmox instance (and for an AWS KMS key to auto-unseal my HashiCorp Vault instance)
- [homelab-ansible](https://github.com/QuantumDancer/homelab-ansible): Ansible configuration for VMs running on Proxmox.
- [packer-vm-template](https://github.com/QuantumDancer/packer-vm-template): RHEL 9 template for Proxmox built by HashiCorp Packer. Does not yet fully work (cloud-init does not pick up networking configuration).
- [homelab-terraform-talos-cluster](https://github.com/QuantumDancer/homelab-terraform-talos-cluster): Terraform configuration for my 3-node Talos Linux Kubernetes Cluster.
- [flux-cluster-config](https://github.com/QuantumDancer/flux-cluster-config): Flux CD based deployments for the Talos Linux cluster. Deprecated. Moved to [idp-argocd-platform-apps](https://github.com/QuantumDancer/idp-argocd-platform-apps).
- [idp-terraform-aws-bootstrap](https://github.com/QuantumDancer/idp-terraform-aws-bootstrap): AWS Landing Zone for my IDP reference implementation
- [idp-argocd-platform-apps](https://github.com/QuantumDancer/idp-argocd-platform-apps): ArgoCD based deployments for my Talos Linux cluster. Focussed on platform engineering tools.
