# Emergency Sheet - Bitwarden Vault Access and 2FA Information

> **Important:** This document contains all information needed to restore access to the Bitwarden vault (password manager), 2FA codes, and backup media. It therefore includes all passwords, 2FA codes for websites, and other security data.
> Print this out and store it in a safe place. Keep at least one additional copy at a different location.
> Created on: _______________

---

## 1. Bitwarden Vault

| Field | Value |
|-------|-------|
| Server | `https://vault.bitwarden.eu` or `https://vault.bitwarden.com` |
| Login email | |
| Master password | |
| Export password | |
| 2FA recovery code | |

> **Note:** The 2FA recovery code does **not** replace the master password.
> Both are required to regain access.

> **Note:** The export password (Backup Passport) is required to decrypt the encrypted JSON export when importing into Bitwarden.

---

## 2. Backing Email (for Bitwarden notifications)

| Field | Value |
|-------|-------|
| Email service (URL) | |
| Email address | |
| Email password | |
| 2FA recovery code | |

---

## 3. Two-Factor Authentication (2FA)

### TOTP App (Ente Auth)

| Field | Value |
|-------|-------|
| Ente Auth email | |
| Ente Auth password | |
| Ente Auth recovery key | |
| Ente export password | |

---

## 4. Backup Encryption

> USB drives are encrypted with VeraCrypt.
> The VeraCrypt password below is required to mount them.

| Field | Value |
|-------|-------|
| VeraCrypt password | |
| USB storage location 1 (home) | |
| USB storage location 2 (offsite) | |

### Cloud Backup (pCloud)

| Field | Value |
|-------|-------|
| pCloud URL | `https://www.pcloud.com` |
| Username / email | |
| Password | |
| Backup-Codes |  |
| Recovery-Codes |  |

> **Note:** The **backup codes** allow access to the pCloud account if the 2FA method is unavailable. Each code can only be used once.

> **Note:** The **recovery codes** allow account recovery if access is completely lost. Each code can only be used once.

---

## 5. Password Pepper (if used)

If passwords are supplemented with a "pepper" after opening the vault:

| Field | Value |
|-------|-------|
| Pepper algorithm / rule | |

---

## 6. Emergency Account (Emergency Access)

A second Bitwarden account configured as emergency access:

| Field | Value |
|-------|-------|
| Server | |
| Login email | |
| Master password | |
| 2FA recovery code | |

> **Note:** Emergency Access requires a waiting period (e.g. 7 days) before access to the main vault is granted. This waiting period must be observed unless the main account holder manually approves access.

---

## 7. Instructions: Vault Access

1. Open a browser and navigate to **vault.bitwarden.com** (or .eu)
2. Log in with the **login email** and **master password** from Section 1
3. Enter the 2FA code (Ente Auth app — see Section 8)

### If 2FA is unavailable

If the Ente Auth app cannot be restored (see Section 8) and no 2FA code is available:

1. On the Bitwarden login page, after entering email and password, click **"Lost your two-step login device?"**
2. Enter the **2FA recovery code** from Section 1
3. Warning: using the recovery code disables 2FA — set it up again afterwards!

### If vault access is completely lost (master password unknown)

- The vault can be deleted at [bitwarden.com/help/forgot-master-password](https://bitwarden.com/help/forgot-master-password/)
- Then restore from backup (Section 9)

---

## 8. Instructions: 2FA Access

### Normal case: use the Ente Auth app

1. Open the **Ente Auth app** on your smartphone
2. Find the **Bitwarden** entry
3. Read the displayed 6-digit code and enter it in the Bitwarden login
4. The code is valid for 30 seconds — if it expires, simply enter the new code

### If the Ente Auth app is lost or unavailable

1. Reinstall **Ente Auth** (App Store or Google Play)
2. Open the app and select **"Restore existing account"**
3. Log in with the **Ente Auth email** and **Ente Auth password** from Section 3
4. Enter the **Ente Auth recovery key** from Section 3 when prompted
5. All 2FA codes will be restored — read the Bitwarden code as in the normal case

### Last resort: restore from encrypted Ente Auth export

If the Ente Auth password and recovery key are both unavailable:

1. Get the encrypted Ente Auth export file from the USB drive (see Section 9, Option A, steps 1–5)
2. Reinstall **Ente Auth** (App Store or Google Play)
3. Open the app and select **"Import"** → choose the export file
4. Enter the **Ente export password** from Section 3 to decrypt the file
5. All 2FA codes will be restored — read the Bitwarden code as in the normal case

---

## 9. Instructions: Backup Access

### Option A: USB drive (VeraCrypt)

1. Insert the USB drive (storage locations: see Section 4)
2. Download and install **VeraCrypt**: [veracrypt.fr](https://www.veracrypt.fr)
3. Open VeraCrypt → **"Mount Volume"** → select the USB drive
4. Enter the **VeraCrypt password** from Section 4
5. Open the mounted drive in Explorer — the backup file (`.json`) is inside
6. Log into Bitwarden → **Settings → Import vault** → select the file → enter the **export password** from Section 1

### Option B: Cloud backup (pCloud)

1. Open a browser and navigate to **pcloud.com**
2. Log in with the credentials from Section 4 (username and password)
3. If 2FA is requested: use the **2FA recovery code** from Section 4
4. Download the backup file (`.json`)
5. Log into Bitwarden → **Settings → Import vault** → select the file → enter the **export password** from Section 1 (VeraCrypt not needed)
