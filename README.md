# Homelab Documentation

This git repository acts as overview of my Homelab configuration.
Due to different technology stacks, the configuration is split into multiple git repositories.

**Note:** All repositories on GitHub are only a mirror. The main work is done on my self-hosted GitLab instance, which has two self-hosted GitLab runners attached and Renovate configured.

## Homelab repositories

- [homelab-terraform](https://github.com/QuantumDancer/homelab-terraform): Terraform configuration to create new VMs on my Proxmox instance (and for an AWS KMS key to auto-unseal my HashiCorp Vault instance)
- [homelab-ansible](https://github.com/QuantumDancer/homelab-ansible): Ansible configuration for VMs running on Proxmox.
- [packer-vm-template](https://github.com/QuantumDancer/packer-vm-template): RHEL 9 template for Proxmox built by HashiCorp Packer. Does not yet fully work (cloud-init does not pick up networking configuration).
- [homelab-terraform-talos-cluster](https://github.com/QuantumDancer/homelab-terraform-talos-cluster): Terraform configuration for my 3-node Talos Linux Kubernetes Cluster.
  This also contains initial cluster configuration (Cilium for networking, ArgoCD).
  I'm using the ArgoCD [app-of-apps pattern](https://argo-cd.readthedocs.io/en/latest/operator-manual/cluster-bootstrapping/#app-of-apps-pattern-alternative) to pull in the rest of the cluster configuration from [idp-argocd-platform-apps](https://github.com/QuantumDancer/idp-argocd-platform-apps).

## IDP repositories

The Homelab is currently used to develop a reference implementation of an internal developer platform (IDP).
See [idp](https://github.com/QuantumDancer/idp) for more information.
