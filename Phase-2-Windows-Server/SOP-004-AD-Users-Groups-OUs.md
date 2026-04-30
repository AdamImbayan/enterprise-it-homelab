# SOP-004: Active Directory Users, Groups and OUs

## Purpose
Create organizational structure in Active Directory
including OUs, users, and security groups.

## Environment
- Domain: lab.local
- Tool: PowerShell (Run as Administrator)

## Steps Completed

### 1. Create Organizational Units
```powershell
New-ADOrganizationalUnit -Name "IT Department" `
-Path "DC=lab,DC=local"

New-ADOrganizationalUnit -Name "HR Department" `
-Path "DC=lab,DC=local"

New-ADOrganizationalUnit -Name "Management" `
-Path "DC=lab,DC=local"
```

### 2. Create Users
```powershell
New-ADUser -Name "John Smith" `
-SamAccountName "jsmith" `
-Path "OU=IT Department,DC=lab,DC=local" `
-Enabled $true

New-ADUser -Name "Sarah Lee" `
-SamAccountName "slee" `
-Path "OU=HR Department,DC=lab,DC=local" `
-Enabled $true
```

### 3. Create Security Groups
```powershell
New-ADGroup -Name "IT-Admins" `
-GroupScope Global `
-Path "OU=IT Department,DC=lab,DC=local"

New-ADGroup -Name "HR-Staff" `
-GroupScope Global `
-Path "OU=HR Department,DC=lab,DC=local"
```

### 4. Add Users to Groups
```powershell
Add-ADGroupMember -Identity "IT-Admins" -Members "jsmith"
Add-ADGroupMember -Identity "HR-Staff" -Members "slee"
```

## Verification
- OUs Created: IT Department, HR Department, Management ✅
- Users Created: jsmith, slee ✅
- Groups Created: IT-Admins, HR-Staff ✅
- Users assigned to groups ✅

## Screenshots
[Add screenshots here]
