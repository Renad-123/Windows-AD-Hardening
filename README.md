# Windows Active Directory Security Hardening

##  Overview
This project demonstrates the installation, configuration, and security hardening of a **Windows Active Directory (AD) Domain Controller** environment, applying multiple **Group Policy Objects (GPOs)** to enforce best security practices.

---

##  Environment Setup
- **Windows Server** (Domain Controller with AD DS installed)
- **Windows Client** (Joined to the domain)

---

##  Implementation Steps

### 1. Environment Preparation
- Installed **Windows Server** and **Windows Client**.
- Installed **Active Directory Domain Services (AD DS)** on the server.
- Promoted the server to a **Domain Controller (DC)**.
- Joined the Windows client machine to the domain.

### 2. Active Directory Structure
- Created **Organizational Units (OUs)** for:
  - Users
  - Computers (Endpoints)
- Added sample users in relevant OUs.

### 3. Security & Group Policy Configuration

#### User & Password Security
- Enforced **Strong Password Policy**.
- Set **Password Expiry** for users.
- Configured **Account Lockout Policy** after multiple failed login attempts.

#### Auditing & Monitoring
- Enabled **Audit Policies** on Domain Controller and client machines.

#### System & User Restrictions
- Enabled **Screensaver Policy** for idle security.
- Disabled unnecessary **services**.
- Applied **Firewall Rules** to block ping to `8.8.8.8` and `8.8.4.4`.
- Disallowed use of **removable media drives**.
- Restricted **software installation**.
- Added **Custom Logon Message**.
- Disabled **CMD** and **PowerShell** access.
- Applied **RDP Restrictions** (limit connections & set idle timeout).
- Disabled **Microsoft Edge InPrivate Mode**.
- Disabled access to **Registry Editor**.
- Prevented installation of **Printer Drivers**.
- Restricted **Time of Day Login** for users.

#### Advanced Security
- Configured **Windows Defender Antivirus** to scan network files.
- Enforced **BitLocker Encryption** on drives.

