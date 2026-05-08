# SOP-003: Active Directory Domain Services Installation

## Purpose
Install and configure Active Directory Domain Services
on Windows Server 2022 to create a lab domain controller.

## Environment
- Server: winserver-lab-01
- Domain: lab.local
- NetBIOS: LAB

## Steps Completed

### 1. Install AD DS Role
- Opened Server Manager
- Add Roles and Features
- Selected Active Directory Domain Services
- Completed installation

### 2. Promote to Domain Controller
- Clicked flag icon in Server Manager
- Selected "Add a new forest"
- Root domain name: lab.local
- Forest/Domain functional level: Windows Server 2016
- DNS Server: Enabled
- Global Catalog: Enabled
- Set DSRM password

### 3. Post-Installation Verification
- Server rebooted automatically
- AD DS role showing green in Server Manager
- DNS role installed automatically
- Verified with PowerShell:
```powershell
Get-ADDomain
netdom query fsmo
```

## Verification
- AD DS Role: Installed ✅
- DNS Role: Installed ✅
- Domain Controller: Promoted ✅
- Domain: lab.local ✅

## Screenshots

### 1. Server Manager — Roles Overview
<img width="1735" height="879" alt="image" src="https://github.com/user-attachments/assets/784dbea7-d3bf-4017-8224-ffcd59d7e278" />


### 2. Installed Roles via PowerShell
<img width="1163" height="576" alt="image" src="https://github.com/user-attachments/assets/745b0829-37d5-48e3-ba03-b45a290d5021" />


### 3. AD Domain Info
<img width="1290" height="556" alt="image" src="https://github.com/user-attachments/assets/0ae79ba1-017e-4159-9fcc-bbfa846054cf" />


### 4. FSMO Roles
<img width="539" height="146" alt="image" src="https://github.com/user-attachments/assets/547f09d0-07df-4d19-94c8-31f021768246" />

### 5. DNS Zones
<img width="986" height="226" alt="image" src="https://github.com/user-attachments/assets/5e840a70-4a7a-46b7-a6d8-2f272eed5f04" />


