
---

# 📂 Backup the Configuration File  ![Badge](https://hitscounter.dev/api/hit?url=https%3A%2F%2Fgithub.com%2Fsohag1192%2FFlussonic-Password-Change-Backup-File&label=Vistors&icon=github&color=%23ff05f7&message=&style=flat&tz=UTC)

Before making any changes to the Flussonic configuration, it is strongly recommended to create a backup. This ensures you can restore the original settings if needed.

## Steps

1. Open a terminal on your server.
2. Run the following command to create a backup copy:
   ```bash
   sudo cp /etc/flussonic/flussonic.conf /etc/flussonic/flussonic.conf.bak
   ```
   - This will save a backup as `flussonic.conf.bak` in the same directory.

3. Verify the backup:
   ```bash
   ls -l /etc/flussonic/flussonic.conf*
   ```
   You should see both the original file and the `.bak` backup.

---

## 🔄 Restore from Backup

If you need to revert to the original configuration:

```bash
sudo mv /etc/flussonic/flussonic.conf.bak /etc/flussonic/flussonic.conf
```

Then reload Flussonic to apply the restored configuration:
```bash
sudo service flussonic reload
```

---

