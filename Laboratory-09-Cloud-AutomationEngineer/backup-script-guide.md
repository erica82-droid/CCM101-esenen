
# Backup Script Guide

## 1. Backup Script Code

The following Bash script automatically compresses the `app-data` directory into a timestamped `.tar.gz` archive stored in the `backups` directory.

```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p "$BACKUP_DIR"

# Compress the source directory into a tarball (.tar.gz)
tar -czf "$BACKUP_DIR/backup_$TIMESTAMP.tar.gz" "$SOURCE_DIR"

echo "Backup completed successfully at $TIMESTAMP!"
```

### How the Script Works

- `#!/bin/bash` tells the system to execute the script using Bash.
- `SOURCE_DIR="app-data"` specifies the directory containing the client's data.
- `BACKUP_DIR="backups"` specifies where the backup archives will be stored.
- `TIMESTAMP=$(date +"%Y%m%d_%H%M%S")` generates a timestamp to make each backup filename unique.
- `mkdir -p "$BACKUP_DIR"` creates the backup directory if it does not already exist.
- `tar -czf` compresses the source directory into a gzip-compressed tar archive.
- `echo` displays messages in the terminal.

## 2. File Permissions: chmod +x

The command `chmod +x backup.sh` adds execute permission to the backup script. This allows the operating system to run the script directly using `./backup.sh`, provided the user also has the necessary access permissions.

Without execute permission, attempting to run the script directly may produce a "Permission denied" error.

## 3. Cron Job Schedule

The cron expression used for the automated backup is:

```bash
0 2 * * * /root/backup.sh
```

This schedules the backup script to run every day at 2:00 AM, based on the system's local time and timezone.

### Breakdown of the Five Time Fields

| Field | Value | Meaning |
|---|---|---|
| Minute | `0` | Runs at minute zero |
| Hour | `2` | Runs at 2 AM |
| Day of Month | `*` | Runs every day of the month |
| Month | `*` | Runs every month |
| Day of Week | `*` | Allows any day of the week |

The final part, `/root/backup.sh`, is the absolute path to the script that cron executes.

## 4. Verification Commands

The following commands were used to test and verify the backup automation:

```bash
chmod +x backup.sh
./backup.sh
ls -l backups/
crontab -l
```

- `chmod +x backup.sh` grants execute permission.
- `./backup.sh` runs the backup script.
- `ls -l backups/` lists the generated backup archives.
- `crontab -l` displays the installed cron schedule.

## 5. Conclusion

This task demonstrates how Bash scripting, file permissions, compressed archives, and cron scheduling can be combined to automate routine backup operations. The solution reduces manual effort and helps the IT team create regularly scheduled copies of important client data.
