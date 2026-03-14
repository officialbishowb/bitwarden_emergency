# Emergency Sheet

> **Wichtig:** Dieses Dokument enthält alle Informationen, um wieder Zugang zum Bitwarden-Vault (Password Manager), wo sich alle Passwörter von Websites und Sicherheitsdaten befinden.
> Ausgedruckt und an einem sicheren Ort aufbewahren. Mindestens eine zweite Kopie an einem anderen Ort lagern.
> Erstellt am: _______________

---

## 1. Bitwarden-Vault

| Feld | Wert |
|------|------|
| Server | `https://vault.bitwarden.eu` oder `https://vault.bitwarden.com` |
| Login-E-Mail | |
| Master-Passwort | |
| 2FA-Recovery-Code |  |

> **Hinweis:** Der 2FA-Recovery-Code ersetzt **nicht** das Master-Passwort.
> Beide werden benötigt, um wieder Zugang zu erhalten.

---

## 2. Backing-E-Mail (für Bitwarden-Benachrichtigungen)

| Feld | Wert |
|------|------|
| E-Mail-Dienst (URL) | |
| E-Mail-Adresse | |
| E-Mail-Passwort | |
| 2FA-Recovery-Code | |

---

## 3. Zwei-Faktor-Authentifizierung (2FA)

### Option A: FIDO2-Hardware-Sicherheitsschlüssel (z.B. Yubikey)

| Feld | Wert |
|------|------|
| Yubikey PIN | |
| Aufbewahrungsort Ersatz-Key | |

### Option B: TOTP-App (Ente Auth)

| Feld | Wert |
|------|------|
| Ente Auth E-Mail | |
| Ente Auth Passwort | |
| Ente Auth Recovery Key | |

---

## 4. Backup-Verschlüsselung

| Feld | Wert |
|------|------|
| Backup-Passwort (6-Wort-Passphrase) | |
| Aufbewahrungsort USB-Laufwerke | |

---

## 5. Passwort-Pepper (falls verwendet)

Falls Passwörter nach dem Öffnen des Vaults noch mit einem "Pepper" ergänzt werden:

| Feld | Wert |
|------|------|
| Pepper-Algorithmus / Regel | |

---
 
## 7. Anleitung zum Vault-Zugang

1. Browser öffnen und zu **vault.bitwarden.com** (oder .eu) navigieren
2. Mit **Login-E-Mail** und **Master-Passwort** aus Abschnitt 1 anmelden
3. 2FA-Code eingeben (Ente Auth App oder Yubikey)
4. Falls 2FA nicht verfügbar: **2FA-Recovery-Code** aus Abschnitt 1 verwenden

Falls der Vault-Zugang komplett verloren gegangen ist (kein Master-Passwort bekannt):
- Vault kann über [bitwarden.com/help/forgot-master-password](https://bitwarden.com/help/forgot-master-password/) gelöscht werden
- Dann Backup einspielen (Abschnitt 4)
