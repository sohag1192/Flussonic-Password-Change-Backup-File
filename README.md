
### 🔧 Method 1: Editing the Configuration File
1. Open the configuration file:
   ```bash
   sudo nano /etc/flussonic/flussonic.conf
   ```
2. Find the `edit_auth` directive. It will look like:
   ```
   edit_auth admin oldpassword
   ```
3. Replace `oldpassword` with your new password.
4. Save and exit the file.
5. Reload the Flussonic configuration to apply changes:
   ```bash
   sudo service flussonic reload
   ```


---

### 🖥️ Method 2: Using the Admin UI
1. Log in to the Flussonic web interface with your current admin credentials.
2. Go to **Settings → Users**.
3. Select the administrator account and update the password.
4. Save changes — no reload is needed.

---

⚠️ **Tips**
- Always use a strong password (letters, numbers, symbols).
- If you edit the config file directly, make sure there are no syntax errors.
- Keep a backup of your configuration file before making changes.

