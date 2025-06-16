# 🗂️ User Permissions & File Sharing Lab (Windows 12)

## 📌 Overview
This lab demonstrates how to configure and test NTFS and shared folder permissions on a standalone Windows 12 system using local user accounts. It simulates real-world help desk tasks like restricting file access, allowing limited permissions, and troubleshooting "Access Denied" errors.

---

## 🧰 Tools Used
- Windows 12 Virtual Machine
- Local User Accounts (`TestUser1`, `TestUser2`)
- NTFS & Share Permissions
- `runas` Command (for simulating different user access)

---

## 🎯 Objectives
- Create and manage local user accounts
- Set up a shared folder with different access levels
- Test permission behavior by switching users
- Simulate common file access issues and troubleshoot them

---

## 🛠️ Steps Performed

### 1. Created Local Users
- `TestUser1`: Full access to shared folder
- `TestUser2`: Read-only access

### 2. Created and Shared Folder
- Folder Path: `C:\SharedFolder`
- Share name: `SharedFolder`
- Share permissions:
  - `TestUser1`: Full Control
  - `TestUser2`: Read

### 3. Configured NTFS Permissions
- `TestUser1`: Full Control
- `TestUser2`: Read & Execute

### 4. Tested Access as Different Users
- Used `runas` and/or Fast User Switching
- Navigated to: `\\localhost\SharedFolder`
- `TestUser1` created and edited a file: `TestFile_User1.txt`
- `TestUser2` was able to view but not modify or delete files

### 5. Simulated "Access Denied"
- Removed all permissions for `TestUser2`
- Attempted access and verified "Access Denied" prompt

---

## 📸 Screenshots

> Include your screenshots in a `/screenshots` folder in the repo and link them below.

- ✅ [User creation in Computer Management](screenshots/user_creation.png)
- ✅ [NTFS permissions for folder](screenshots/ntfs_permissions.png)
- ✅ [Share settings](screenshots/share_settings.png)
- ✅ [File creation by TestUser1](screenshots/testuser1_create.png)
- ✅ [TestUser2 denied edit/delete](screenshots/testuser2_denied.png)
- ✅ [Access Denied error](screenshots/access_denied.png)

---

## 🔑 Key Takeaways
- NTFS permissions are more granular and override Share permissions when more restrictive.
- You can simulate enterprise-like permission scenarios using local accounts.
- This setup mirrors basic help desk tasks like managing file access and resolving permission issues.



