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
[Add screenshots here]
