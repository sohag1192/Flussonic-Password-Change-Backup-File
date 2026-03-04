---

# Flussonic Administrator Password Management  ![Badge](https://hitscounter.dev/api/hit?url=https%3A%2F%2Fgithub.com%2Fsohag1192%2FFlussonic-Password-Change-Backup-File&label=Vistors&icon=github&color=%23ff05f7&message=&style=flat&tz=UTC)

This guide explains how to change the administrator’s password in Flussonic. You can update the password either by editing the configuration file or through the Admin UI.

---

## 🔧 Method 1: Editing the Configuration File

1. Open the Flussonic configuration file:
   ```bash
   sudo nano /etc/flussonic/flussonic.conf
   ```

2. Locate the `edit_auth` directive. It will look like:
   ```
   edit_auth admin oldpassword
   ```

3. Replace `oldpassword` with your new password.

4. Save and exit the file.

5. Reload the Flussonic configuration to apply changes:
   ```bash
   sudo service flussonic reload
   ```
   or
   ```bash
   sudo config back
   ```

---

## 🖥️ Method 2: Using the Admin UI

1. Log in to the Flussonic web interface with your current admin credentials.
2. Navigate to **Settings → Users**.
3. Select the administrator account and update the password.
4. Save changes.  
   *(No service reload is required when using the UI.)*

---

## ⚠️ Notes & Best Practices

- Always choose a strong password (uppercase, lowercase, numbers, symbols).
- Keep a backup of your configuration file before making changes.
- Ensure there are no syntax errors in `flussonic.conf` — otherwise, the server may fail to reload.
- Consider creating a secondary admin account for recovery purposes.

---


Reference: https://flussonic.com/doc/admin/installation/#installation-password-change


