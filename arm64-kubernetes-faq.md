# Project archived

Lots has changed from 2018 when this started, and the FAQ
has not kept up. This project is now archived.

# Frequently asked questions about Kubernetes on arm64, with answers

Edited by Ed Vielmetti, Packet, Works on Arm project ed@packet.net

See below for a complete list of contributors.

### About this document

This FAQ is designed to capture the questions that come up in the #arm64
channel, and to provide answers and links to writeups and tutorials that 
answer those questions.

Pull requests are welcomed.

## Table of contents

* Basics
* Hardware choices
* Provisioning tools
* Memory considerations
* Networking
* Mixed architecture clusters

### Hardware choices

* 32-bit vs 64-bit clusters
* Raspberry Pi
* Rock64
* Cavium ThunderX

### Provisioning tools

* [Ansible](#ansible)
* Pharmer
* Kontena Pharos

### Memory considerations

* Running etcd on a separate node

### Networking

* Weave
* Flannel
* MetalLB (load balancer for bare metal)
* Calico

### Applications

* OpenFaaS
* Gitlab CI

### Mixed architecture clusters

--

## Ansible

Ansible is a configuration management and provisioning tool written
in Python that uses SSH to update remote configuraitons. Ansible
playbooks automate setup of systems.

Chris Short has `rak8s` (pronounced rackets), an Ansible playbook to deploy Kubernetes to Raspberry Pis.

* https://chrisshort.net/my-raspberry-pi-kubernetes-cluster/
* https://rak8s.io/
* https://github.com/rak8s/rak8s

Michael Robbins has a set of Ansible playbooks for setting up a
Raspbian Stretch (32-bit) cluster.

* https://github.com/michael-robbins/rpi-k8s-ansible

Citrullin has a set of Ansible playbooks for setting up an arm64
cluster in an all-IPv6 configuration.

* https://github.com/Citrullin/ansible-kubernetes-arm-ipv6

--

### Credits

Thanks to the following for their contributions:

* Carl Perry
* Chris Short
* Michael Robbins
* Josh Reichardt

