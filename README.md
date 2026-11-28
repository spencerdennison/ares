# olympus

Configuration for my workstations.

## Table of Contents   

* [Pre-Installation](#pre-installation)
* [Installation](#installation)
* [Post-Installation](#post-installation)

## Pre-Installation

- Install Arch on workstation

## Installation

Update and upgrade pacman package repository

```bash
sudo pacman -Syu
```

Install Ansible and Git

```bash
sudo pacman -S ansible git
```

Clone repository

```bash
git clone https://github.com/spencerdennison/olympus.git
```

Change directory to olympus

```bash
cd olympus
```

Run Ansible playbooks

```bash
./scripts/provision.sh
```

## Post-Installation

Generate SSH keys

```bash
ssh-keygen -t ed25519 -f ~/.ssh/key
```

Add hermes to Tailscale network

```bash
sudo tailscale up
```

Reboot workstation

```bash
sudo reboot
```
