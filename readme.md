# Kubernetes self-hosted test on Vagrant
2020.02.09

## Purpose
- learn Kubernetes components by installing it
  - following guides here: https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/

## Details
So far this repo provides:
- Vagrantfile   - to quickly spin up multiple identical nodes
- inventory.yaml    - inventory file for ansible playbook
- 01-install-packages   - ansible playbook to prep the node and install all the software dependencies for kubernetes

## Usage

    # first, spin up the VMs
    > vagrant up
    
    # this will install software dependencies
    > ansible-playbook -i inventory.yaml 01-install-packages.yaml
