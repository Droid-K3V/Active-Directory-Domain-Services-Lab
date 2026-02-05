# Active Directory Domain Services (AD DS) Lab
A complete, end-to-end Windows Server Active Directory environment built from scratch.
This project demonstrates domain creation, user/group management, workstation domain join, Group Policy enforcement, and real troubleshooting.
---
## 🏗️ Lab Architecture
**Domain Controller:**
 - Windows Server 2019
 - Hostname: DC01
 - Domain: kevinlab.local
 - Roles Installed: Active Directory Domain Services DNS
**Client Workstation:**
 - Windows 10 Pro
 - Joined to kevinlab.local
 - Used for GPO testing and user login validation
**Organizational Units:**
- Chicago
  - Users
  - Workstations
  - Security Groups

## 👤 User & Group Management
Created domain users and security groups to simulate a real enterprise environment:
- Standard Users
- Admin Accounts
- Department-based security groups
- Password Policies
- Login verification on Windows 10 client

# 🖥️ Workstation Domain Join
A Windows 10 VM was joined to the domain:
- Configured DNS to point to DC01
- Joined the domain successfully
- Verified domain login with user accounts
- Confirmed workstation appears under **Chicago -> Workstation**

## 🛡️ Group Policy Objects (GPOs)
Multiple GPOs were created and linked to the correct OUs:

### ✔️ User-Side GPOs
- Desktop restrictions
- Wallpaper enforcement (policy applied successfully; fallback color confirmed)

### ✔️ Computer-Side GPOs
- Security hardening
- Windows Update configuration
- Login message banner
- Password policy enforcement

## 🧪 GPO Verification
All GPOs were validated on the Windows 10 client using:
- gpupdate /force
- gpresult /r
Wallpaper GPO applied (background changed to fallback color, confirming enforcement).
Other GPOs applied successfully and are documented with screenshots.

## 🧶 Troubleshooting & Lessons Learned
This project included real-world troubleshooting:
- SYSVOL/NETLOGON behavior
- GPO replication
- Wallpaper fallback behavior
- DNS misconfiguration
- Domain Join issues
- OU linking mistakes
- GPO precedence and inheritance
Each issue was documented and resolve, demonstrating practical AD DS experience.

## 🏁 Final Result
A fully functional Active Directory environment with:
- Domain controller
- DNS
- Organizational structure
- Users & Groups
- Domain-joined workstation
- Working GPOs
- Verified policy enforcement
- Complete documentation and screenshots
This project reflects real enterprise administration skillsand hands-on troubleshooting.
