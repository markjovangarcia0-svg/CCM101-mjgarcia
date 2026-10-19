# Backup Script Guide

## 1. Purpose

The backup script automates the process of creating a compressed backup of application data. It reduces manual work and helps protect important files.

## 2. Source and Destination

- **Script location:** `/root/backup.sh`
- **Source directory:** `/root/app-data`
- **Backup directory:** `/root/backups`
- **Backup format:** `.tar.gz`

The script uses a timestamp in each backup filename so that backups created at different times can be distinguished.

## 3. Script Explanation

- `#!/bin/bash` identifies Bash as the script interpreter.
- `SOURCE_DIR="app-data"` specifies the folder to back up.
- `BACKUP_DIR="backups"` specifies where the archive will be stored.
- `TIMESTAMP=$(date +"%Y%m%d_%H%M%S")` generates a date-and-time value.
- `mkdir -p "$BACKUP_DIR"` creates the backup directory if it does not exist.
- `tar -czf` compresses the source directory into a `.tar.gz` archive.
- `echo` displays messages in the terminal.

## 4. Permissions and Execution

Make the script executable:

```bash
chmod +x /root/backup.sh
```

Run it from the root directory:

```bash
cd /root
./backup.sh
```

## 5. Verify the Backup

List the generated archives:

```bash
ls -lh /root/backups/
```

Inspect the contents of an archive:

```bash
tar -tzf /root/backups/backup_*.tar.gz
```

The output should include the application data file.

## 6. Cron Schedule

The scheduled entry is:

```cron
0 2 * * * /root/backup.sh
```

The five Cron fields represent:

| Field | Value | Meaning |
|---|---|---|
| Minute | `0` | At minute zero |
| Hour | `2` | At 2 AM |
| Day of month | `*` | Every day of the month |
| Month | `*` | Every month |
| Day of week | `*` | Every day of the week |

Check the installed schedule using:

```bash
crontab -l
```

## 7. Important Notes

The script should be tested before being used for important data. Backup archives should also be checked regularly, stored securely, and copied to a separate location when possible. A successful command alone does not guarantee that a backup can be restored.
