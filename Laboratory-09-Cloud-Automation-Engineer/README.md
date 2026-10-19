# Laboratory 09 – The Cloud Automation Engineer

## Mission Overview

This laboratory explores how Bash scripts and Cron jobs can automate routine cloud administration tasks. The activity focuses on creating a backup script, running it, verifying the generated archive, and scheduling it to execute daily.

## Objectives

- Understand the purpose of Bash scripts and variables.
- Create a compressed backup of application data.
- Set executable permissions on a Bash script.
- Verify the generated backup archive.
- Schedule a recurring task using Cron.
- Document the procedure and reflect on the importance of automation.

## Commands Executed

```bash
mkdir -p /root/app-data
echo "This is critical client data." > /root/app-data/data.txt
nano /root/backup.sh
chmod +x /root/backup.sh
cd /root
./backup.sh
ls -lh /root/backups/
tar -tzf /root/backups/backup_*.tar.gz
crontab -l
env EDITOR=nano crontab -e
```

## Skills Learned

- Writing and executing Bash scripts.
- Using variables and timestamps.
- Creating compressed archives with `tar`.
- Managing script permissions.
- Scheduling tasks with Cron.
- Checking backup files and documenting technical procedures.

## Evidence

The `screenshots/` folder contains the two required screenshots:

1. `script-execution.png` – Shows successful backup execution and the generated archive.
2. `cron-schedule.png` – Shows the installed daily Cron schedule.

## Result

The backup script was tested against sample application data, and a Cron entry was configured to run it daily at 2:00 AM. The activity demonstrates how automation can reduce repetitive work and support regular data protection.
