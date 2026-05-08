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

### 1. Organizational Units (OUs)
<img width="988" height="194" alt="image" src="https://github.com/user-attachments/assets/170a5aa9-95a4-4993-8c0d-caeb6db2385c" />


### 2. AD Users List
<img width="982" height="170" alt="image" src="https://github.com/user-attachments/assets/d65e4701-a280-4ae4-b4ed-f5df6ff08add" />


### 3. AD Groups List
<img width="722" height="879" alt="image" src="https://github.com/user-attachments/assets/14446116-e31f-4298-9f7c-21fcc6d0a3b0" />


### 4. IT-Admins Group Members
<img width="586" height="163" alt="image" src="https://github.com/user-attachments/assets/a3c198ce-bdea-4656-9dfd-4de470216d71" />


### 5. HR-Staff Group Members
<img width="586" height="163" alt="image" src="https://github.com/user-attachments/assets/210c5737-57c0-4212-82bd-8e9c144c27a5" />


### 6. Active Directory Users and Computers (GUI)
<img width="1120" height="568" alt="image" src="https://github.com/user-attachments/assets/5736222c-e686-453e-8e49-a44c20ee5c15" />

### 7. IT Department OU:
<img width="1120" height="568" alt="image" src="https://github.com/user-attachments/assets/561a1c76-4f59-4ae9-b6df-6f5e9c46c606" />

### 8. — HR Department OU:
<img width="1120" height="568" alt="image" src="https://github.com/user-attachments/assets/441eb7f3-4fbc-4432-8441-54f66e87c55b" />
