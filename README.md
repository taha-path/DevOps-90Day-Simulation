🚀 90-Day DevOps Job Simulation: Day 01
Automated Multi-Node Lab Infrastructure
This repository contains the foundation for a professional DevOps lab, built using Infrastructure as Code (IaC) principles. It automates the creation of a 3-node Linux cluster to simulate a production-grade environment.

🛠️ Tech Stack
Orchestration: Vagrant

Virtualization: VirtualBox 7.2

OS: Ubuntu 22.04 LTS (Jammy Jellyfish)

Provisioning: Bash Scripting

Tools Installed: Docker, Kubectl, Terraform

🏗️ Architecture
The lab consists of three virtual machines with static networking:

k8s-master: 192.168.56.10 (2 vCPU, 2GB RAM)

k8s-worker-01: 192.168.56.31 (2 vCPU, 2GB RAM)

k8s-worker-02: 192.168.56.32 (2 vCPU, 2GB RAM)

🚀 Getting Started
Clone the repo: git clone https://github.com/Taha-path/DevOps-90Day-Simulation.git

Launch the lab: Navigate to the folder and run vagrant up.

Access nodes: Use vagrant ssh master or vagrant ssh web01.

📁 Project Structure
Vagrantfile: Defines the virtual hardware and network.

BashScript/bootstrap.sh: Automates the installation of the DevOps toolchain on every boot.
