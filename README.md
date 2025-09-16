🛠️ Ansible Setup & Playbooks on Fedora/CentOS
📘 Overview
This repository contains instructions and playbooks for installing and using Ansible on Fedora-based Linux systems (including CentOS). It includes basic setup, configuration file management, and a sample playbook to get started with automation.

📦 Installation Steps


Shell
# Install EPEL and Ansible
sudo dnf install epel-release
sudo dnf install ansible

# Verify installation
ansible localhost -m ping

⚙️ Configuration Files
Ansible's default configuration and inventory files are located at:

/etc/ansible/ansible.cfg
/etc/ansible/hosts
🔍 View or Initialize Config:



Shell
cd /etc/ansible/
less ansible.cfg

# Generate a full config template with all options disabled
ansible-config init --disabled -t all > ansible.cfg
less ansible.cfg

📂 Creating Your First Playbook



Shell
cd /etc/ansible
mkdir playbooks
cd playbooks
vi first_pb.yml

📝 Sample Playbook: first_pb.yml



YAML
---
- name: Test Playbook
  hosts: localhost
  tasks:
    - name: Ping localhost
      ping:

📁 Repository Structure
ansible-fedora-setup/
├── README.md
├── playbooks/
│   └── first_pb.yml
└── ansible.cfg
📌 Requirements
Fedora/CentOS Linux
Ansible 2.9+
Python 3.x
SSH access (for remote hosts)
