# Descomplicando Kubernetes

A repository to simplify Kubernetes setup and configuration using Vagrant and Docker.

## Overview

This project provides scripts and configuration files to quickly set up a Kubernetes cluster using Vagrant virtual machines. It automates the process of creating VMs, installing Docker, and configuring the necessary components for Kubernetes.

## Prerequisites

- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- [Vagrant](https://www.vagrantup.com/downloads)
- Sufficient RAM and CPU resources to run multiple VMs

## Getting Started

1. Clone this repository:
   ```bash
   git clone https://github.com/thiago733/descomplicandoKubernetes.git
   cd descomplicandoKubernetes
   ```

2. Start the Vagrant environment:
   ```bash
   vagrant up
   ```

## VM Configuration

The [Vagrantfile](Vagrantfile) defines three virtual machines:

- **kube01**: Master node with 4 CPUs and 4GB RAM
- **kube02**: Worker node with 2 CPUs and 2GB RAM
- **kube03**: Worker node with 2 CPUs and 2GB RAM

## Utility Scripts

- [AtualizaOSviaAPT.sh](AtualizaOSviaAPT.sh): Updates the OS packages
- [InstalaDocker.sh](InstalaDocker.sh): Installs Docker
- [HabilitaSystemDnoDocker.sh](HabilitaSystemDnoDocker.sh): Configures Docker to use systemd as the cgroup driver

## Kernel Module Configuration

The [k8s.conf](etc/modules-load.d/k8s.conf) file in the `etc/modules-load.d` directory configures the necessary kernel modules for Kubernetes.

## License

This project is open source and available under the terms of the MIT license.
