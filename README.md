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
- ✅ [User creation in Computer Management]

<img width="987" alt="creating new users action in computer management" src="https://github.com/user-attachments/assets/b937681b-2d87-4bd2-a9dd-a00f54987347" />

<img width="985" alt="creating test2 user" src="https://github.com/user-attachments/assets/217c3fb6-0f6b-44e6-8482-4b75fe2b82d8" />

<img width="978" alt="creating shared folder wizard" src="https://github.com/user-attachments/assets/8c3cf329-d12d-4159-b1b4-2058c2237961" />

<img width="986" alt="sucessful shared wizard" src="https://github.com/user-attachments/assets/90bb54be-cdca-44cb-9721-eabb66917af9" />

<img width="990" alt="adding users in shared folder" src="https://github.com/user-attachments/assets/6f47b8c8-90c6-4edd-8979-9252e7d8f7cc" />

<img width="985" alt="sharedfolder location" src="https://github.com/user-attachments/assets/8328680a-cfc1-47d7-8d49-b6573299c6ab" />

<img width="986" alt="shared folder pathway" src="https://github.com/user-attachments/assets/08292c03-52ef-440e-9475-18a4c792ab38" />

- ✅ [NTFS permissions for folder]
  
<img width="986" alt="test1 customization perm" src="https://github.com/user-attachments/assets/2b876004-5ce7-446c-9f0f-f88aeb146fcc" />

<img width="982" alt="Test2 custom perm" src="https://github.com/user-attachments/assets/4059ff1b-c667-4a84-adb6-dd6b0db09dc7" />

<img width="993" alt="customizing permissions for users" src="https://github.com/user-attachments/assets/3aa0264d-c571-4c4e-92b8-5d5b18c0f330" />

- ✅ [Share settings]

<img width="980" alt="sharedfolder properties test2" src="https://github.com/user-attachments/assets/ab04e19d-33c8-486a-9fd9-be076845aafe" />

<img width="988" alt="sharedfolder properties full control test1" src="https://github.com/user-attachments/assets/3ac099c7-e179-4707-825b-66e07dff7143" />


- ✅ [File creation by TestUser1]

<img width="979" alt="file creation" src="https://github.com/user-attachments/assets/a5597607-acc1-440d-98e2-734dbb031ed7" />

<img width="1000" alt="file1 txt" src="https://github.com/user-attachments/assets/73795cf0-a2e7-44e0-8842-d68091d2ebea" />

<img width="981" alt="file created and viewing" src="https://github.com/user-attachments/assets/c423cd71-3eda-4fd1-bbc7-ac344f67944a" />


- ✅ [TestUser2 denied edit/delete]

<img width="977" alt="denied access" src="https://github.com/user-attachments/assets/c2da9ebf-3594-47ea-b010-e0ec986f29cc" />

---

## 🔑 Key Takeaways
- NTFS permissions are more granular and override Share permissions when more restrictive.
- You can simulate enterprise-like permission scenarios using local accounts.
- This setup mirrors basic help desk tasks like managing file access and resolving permission issues.



