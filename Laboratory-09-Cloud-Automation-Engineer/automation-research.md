# Automation Research

## 1. What Is a Bash Script?

A Bash script is a file that contains Linux commands that run in sequence. It helps automate repeated tasks instead of requiring a user to enter every command manually. The `#!/bin/bash` line, called the shebang, tells the system to use Bash to interpret the script.

## 2. What Are Variables?

Variables store values that can be reused in a script. In the backup script, `SOURCE_DIR` identifies the folder containing the data, while `BACKUP_DIR` identifies where the backup files will be stored. The `TIMESTAMP` variable adds the current date and time to the backup filename. Variables make scripts easier to read, maintain, and update.

## 3. What Is a Cron Job?

A Cron job is a scheduled task in Linux that automatically runs a command at a specified time or interval. It is useful in cloud computing because it can automate regular tasks such as backups, log cleanup, and system maintenance. The Cron expression `0 2 * * *` means the task runs at 2:00 AM every day.

## 4. Why Is Automation Important in Cloud Computing?

Automation reduces repetitive manual work, saves time, and helps tasks run consistently. For example, an automated backup script can protect important application data without requiring an administrator to start the backup manually every day. However, automated tasks must be tested and monitored to ensure they work correctly.
