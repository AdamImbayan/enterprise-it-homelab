# SOP-002: Windows Server 2022 Setup on Azure

## Purpose
Deploy and configure Windows Server 2022 on Azure
for Active Directory lab environment.

## Environment
- Platform: Microsoft Azure
- OS: Windows Server 2022 Datacenter x64 Gen2
- VM Name: winserver-lab-01
- Region: Southeast Asia
- Size: Standard D2s v3 (2 vCPU, 8GB RAM)
- Public IP: 20.191.147.211

## Steps Completed

### 1. VM Deployment
- Created resource group: winserver-lab-01_group
- Deployed Windows Server 2022 Datacenter x64 Gen2
- Configured RDP (port 3389) inbound rule
- Set admin username: labadmin

### 2. Cost Management
- Created budget alert at $10
- Set auto-shutdown at 11:00 PM daily
- Always stop VM via Azure Portal after sessions

### 3. Remote Access
- Connected via RDP using Remmina on Linux laptop
- Verified successful login to Windows Server desktop

## Verification
- VM Status: Running ✅
- RDP Access: Working ✅
- Auto-shutdown: Configured ✅

## Screenshots

### 1. VM Overview - Azure Portal
<img width="1340" height="294" alt="image" src="https://github.com/user-attachments/assets/b76353b0-5b91-4553-9db5-53f3b1616ba3" />


### 2. Auto-Shutdown Configuration
<img width="1329" height="387" alt="image" src="https://github.com/user-attachments/assets/20e51edf-bf23-4603-8fec-0092eda676f8" />


### 3. Network Settings - RDP Port 3389
<img width="1496" height="783" alt="image" src="https://github.com/user-attachments/assets/45524557-17ae-433c-8378-4dfb2af397b7" />


### 4. Server Manager Dashboard
<img width="1917" height="1031" alt="image" src="https://github.com/user-attachments/assets/20cabd75-6961-436d-94a9-b764ed922ac1" />
