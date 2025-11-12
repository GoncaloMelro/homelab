# Homelab

This repository contains configuration and notes for my home lab.

## Introduction

I created this home lab to learn, experiment, and try different tools. It runs on an old laptop with a broken keyboard (8 GB RAM, 500 GB SSD). I installed the latest Ubuntu Server and did not use LVM.

## Current setup
- Docker installed
- Immich deployed
- System adjustments (for example, prevent suspend when the laptop lid is closed)
- SSH configured
- DHCP/static IP configured to ensure a consistent address for the server

Everything related to the server itself, should be self decumented by ansible itself

## Ansible

I want to use Ansible to manage the setup as infrastructure-as-code. It will be useful for repeatable configuration and documentation.

Prerequisites:
```bash
sudo apt update
sudo apt install ansible sshpass -y
```

Common command (dry run):
```bash
ansible-playbook playbooks/site.yml -i hosts.in --check -k -K
```
Remove `--check` to apply changes.

## Planned work
- Configure Grafana e make a dashboard for
    - server use stats (1860 dashboard)
    - immich
- File manager (samba or just something more robust)
- Configure Pi-hole (for fun and ad blocking)
- Create a personal web server with a custom dashboard
- Expose services securely (via a VPN)
- Explore useful Docker images
- Configure a reverse proxy
- Enable Wake-on-LAN (power on the server via Ethernet to save energy)
