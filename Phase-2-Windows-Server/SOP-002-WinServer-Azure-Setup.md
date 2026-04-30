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
[Add screenshots here]
