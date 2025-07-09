# Homelab Kubernetes Cluster with Ansible and Vagrant

This project sets up a local multi-node Kubernetes cluster using **Vagrant**, **VirtualBox**, and **Ansible** — all running from a Windows 11 host.

It’s designed for testing, learning and simulating production-like environments locally.

---

## Features

- 🖥️ Virtual machines provisioned via **Vagrant** and **VirtualBox**
- ⚙️ Kubernetes 3-node cluster via **kubeadm** (`1 master`, `2 workers`)
- 🔁 Cluster bootstrapped entirely using **Ansible**
- 📦 Uses `containerd` as the container runtime
- 🧪 Ready for testing CI/CD, observability, Helm, and more

---

## Technologies Used

- **Host:** Windows 11 (with WSL running Ansible)
- **VMs:** Ubuntu 22.04 (via `ubuntu/jammy64` Vagrant box)
- **Virtualization:** VirtualBox
- **Provisioning:** Vagrant + Ansible
- **Orchestration:** Kubernetes (via kubeadm)
- **CNI:** Flannel (default)
- **Ansible roles/playbooks:** Structured and reusable
