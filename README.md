# 🔐 Enable TPM, Secure Boot, and UEFI in VMware Workstation

This document explains how to enable:

* **UEFI Firmware**
* **Secure Boot**
* **Trusted Platform Module (TPM)**

in **VMware Workstation** for a virtual machine (example: **Windows 10 VM**).

This configuration is required for operating systems that require **hardware security features**, such as **Windows 11** or enhanced security environments.

---

# 📋 Prerequisites

Before starting, ensure the following:

* VMware Workstation is installed
* A virtual machine already exists (example: **Windows 10 VM**)
* Administrative access to modify VM settings

⚠️ **Important Note**

VMware requires the **virtual machine to be encrypted** before adding a **Trusted Platform Module (TPM)**.

---

# 🖥 Step 1 — Open VMware Workstation

1. Launch **VMware Workstation**.
2. Locate the virtual machine you want to configure.

Example:

```
Virtual Machine: Windows 10
```

---

# ⚙️ Step 2 — Enable UEFI Firmware and Secure Boot

1. Right-click the virtual machine.

```
Right Click → Settings
```

2. Navigate to:

```
Options → Advanced
```

3. Under **Firmware Type**, select:

```
UEFI
```

4. Enable the following option:

```
✔ Enable Secure Boot
```

5. Click **OK** to apply the configuration.

---

# 🧩 Step 3 — Attempt to Add Trusted Platform Module (TPM)

1. Right-click the virtual machine again.

```
Right Click → Settings
```

2. Navigate to:

```
Hardware → Add
```

3. Select:

```
Trusted Platform Module
```

4. Click **Finish**.

---

# ⚠️ Issue: Finish Button is Disabled

In many cases, the **Finish button will appear greyed out and cannot be clicked**.

This occurs because:

> VMware requires the virtual machine to be **encrypted before adding TPM hardware**.

If the **Finish button is disabled**, click:

```
Cancel
```

---

# 🔒 Step 4 — Encrypt the Virtual Machine

To enable TPM support, the virtual machine must be encrypted.

1. Right-click the virtual machine.

```
Right Click → Settings
```

2. Navigate to:

```
Options → Access Control
```

3. The status will show:

```
Not encrypted
```

4. Click:

```
Encrypt
```

---

# 🔑 Step 5 — Configure Encryption

The **Encrypt Virtual Machine** dialog box will appear.

Select the following option:

```
Only the files needed to support a TPM are encrypted
```

Enter the encryption password.

Example:

```
Password: Password@123
Confirm: Password@123
```

---

# 💾 Step 6 — Save Password in Credential Manager

Enable the following option:

```
✔ Remember the password on this machine in Credential Manager
```

Then click:

```
Encrypt
```

Wait for the encryption process to complete.

---

# 🧩 Step 7 — Add Trusted Platform Module (TPM)

After encryption is completed:

1. Right-click the virtual machine again.

```
Right Click → Settings
```

2. Navigate to:

```
Hardware → Add
```

3. Select:

```
Trusted Platform Module
```

4. Click **Finish**.

---

# ✅ Step 8 — Verification

After completing the process, you should see:

```
Trusted Platform Module : Present
```

This confirms that the **TPM device has been successfully added** to the virtual machine.

---

# 🎉 Result

Your virtual machine now has the following security features enabled:

✔ UEFI Firmware
✔ Secure Boot
✔ Trusted Platform Module (TPM)

These features are required for modern operating systems and enhanced system security.

---
