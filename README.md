# ☸️ Hybrid K3s Homelab Infrastructure

Infrastructure as Code (IaC) repository for bootstrapping a hybrid Kubernetes cluster (AMD64 + ARM64) using **Ansible** and **K3s**.

## 🏗 Architecture

| Role | Device | Specs | OS | Arch |
| :--- | :--- | :--- | :--- | :--- |
| **Master Node** | HP Elitedesk | 16GB RAM | Ubuntu Server 24.04 | `amd64` |
| **Worker Node** | Raspberry Pi 5 | 4GB RAM | Raspberry Pi OS Lite | `arm64` |
| **Worker Node** | Raspberry Pi 4B | 4GB RAM | Raspberry Pi OS Lite | `arm64` |

## 🛠 Tech Stack
* **Ansible:** Configuration Management & Automation.
* **K3s:** Lightweight Kubernetes distribution suitable for Edge/IoT.
* **Tailscale:** Mesh VPN for secure inter-node communication.

## 🚀 Features
This Ansible setup automates the "Zero to Hero" process:
1. **System Prep:** Disabling swap, configuring cgroups for ARM64 containers.
2. **Networking:** Installing and authenticating Tailscale VPN.
3. **Cluster Bootstrap:** Installing K3s Master and joining Worker nodes automatically.
4. **Local Access:** Fetching `kubeconfig` to the local developer machine for immediate access.
