# SOP-001: Ubuntu Server 24.04 Setup & Hardening

## Purpose
Set up and harden an Ubuntu Server 24.04 LTS VM 
on Proxmox for enterprise lab use.

## Environment
- Hypervisor: Proxmox VE 9.1.1
- OS: Ubuntu Server 24.04 LTS
- VM Name: ubuntu-lab-01

## Steps Completed

### 1. System Installation
- Installed Ubuntu Server 24.04 LTS on Proxmox VM
- Enabled OpenSSH during installation

### 2. System Update
```bash
sudo apt update && sudo apt upgrade -y
```

### 3. SSH Hardening
```bash
sudo nano /etc/ssh/sshd_config
```
Changes made:
- PermitRootLogin no
- MaxAuthTries 3
- X11Forwarding no

```bash
sudo systemctl restart ssh
```

### 4. UFW Firewall Setup
```bash
sudo apt install ufw -y
sudo ufw allow ssh
sudo ufw enable
sudo ufw status
```

### 5. Fail2ban Installation
```bash
sudo apt install fail2ban -y
sudo systemctl enable fail2ban
sudo systemctl start fail2ban
```

## Verification
- UFW Status: Active ✅
- fail2ban Status: Active ✅
- SSH root login: Disabled ✅
- fail2ban sshd jail: Active ✅

## Result
Ubuntu Server successfully hardened and secured
for lab use.

# 1. System info
<img width="988" height="57" alt="image" src="https://github.com/user-attachments/assets/60f239b4-7e8a-490d-a6e3-10af683d6908" />

# 2. UFW status
<img width="666" height="195" alt="image" src="https://github.com/user-attachments/assets/b9f8cf27-27e6-40ac-8957-1c13f79c6332" />

