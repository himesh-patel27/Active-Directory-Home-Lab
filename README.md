# 🛡️ Active Directory Home Lab

## 📌 Project Overview

This project involved building a self-contained Active Directory domain environment to practice and demonstrate core Windows Server administration skills — domain controller deployment, user/OU provisioning, Group Policy configuration, and simulated help desk ticket resolution — the most commonly tested skills in entry-level Help Desk / IT Support interviews.

## 🗂️ Lab Environment

- **Hypervisor:** Oracle VirtualBox
- **Domain Controller:** Windows Server 2022 Standard (Evaluation) — Desktop Experience
- **Client Machine:** Windows 11 Enterprise (Evaluation) *(substituted for Windows 10 Enterprise, no longer available for download)*
- **Domain:** `homelab.local`
- **Tools:** PowerShell, Active Directory Users and Computers (ADUC), Group Policy Management Console (GPMC)

## 🛠️ Configuration Steps

1. **VM Creation** – Built two VMs in VirtualBox: `DC01` (Windows Server 2022) and `CLIENT01` (Windows 11 Enterprise)
2. **Server Install & Promotion** – Installed Windows Server 2022 with Desktop Experience, added the AD DS role, and promoted DC01 to a domain controller as the root of a new forest (`homelab.local`)
3. **OU & User Provisioning** – Created Organizational Units (IT, HR, Finance) in ADUC and populated each with test users, requiring password changes at next logon
4. **Group Policy Configuration** – Created a "Disable USB Storage" GPO applied to the IT OU (denies all removable storage classes) and a "Desktop Wallpaper Policy" GPO applied to the HR OU
5. **Domain Join** – Joined CLIENT01 to `homelab.local` and confirmed login with a domain test-user account
6. **Simulated Help Desk Tickets** – Documented three ticket scenarios: account lockout resolution, new-employee onboarding, and password reset
7. **Automation** – Wrote a PowerShell script (`scripts/bulk-user-creation.ps1`) to bulk-provision AD users

## 🔑 Key Learnings

- Started the DC01 install with Server Core, then switched to Desktop Experience after realizing GUI tools (ADUC, GPMC) would make AD management significantly easier to demonstrate and troubleshoot
- Adapted the lab to use Windows 11 Enterprise instead of Windows 10 Enterprise (no longer available); domain-join behavior is identical between the two
- Gained hands-on practice with how AD DS, OUs, and Group Policy work together to manage a real organizational structure
- Practiced the exact ticket types (lockouts, provisioning, password resets) most common in Help Desk roles

## 📂 Files

- `screenshots/` – Screenshots of each major configuration step (DC setup, GPO config, user creation, client domain join)
- `docs/ticket-simulations.md` – Write-ups of the three simulated help desk tickets
- `scripts/bulk-user-creation.ps1` – PowerShell script for bulk AD user provisioning
