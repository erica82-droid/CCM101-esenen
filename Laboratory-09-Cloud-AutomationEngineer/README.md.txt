# Laboratory 09 - Cloud Automation Engineer

## 1. Mission Overview

The mission of this laboratory is to develop a simple automated backup solution using Bash scripting and Linux cron scheduling. The script backs up sample client data by compressing it into a timestamped `.tar.gz` archive, while cron is configured to run the script automatically every day at 2:00 AM.

## 2. Objectives

- Understand the fundamentals of Bash scripting and Linux automation.
- Create a sample client data directory and test file.
- Write a Bash script to compress and back up data.
- Apply executable permissions using `chmod +x`.
- Schedule an automated backup using a cron job.
- Verify the generated backup archive and installed cron schedule.
- Document the implementation for future maintenance.

## 3. Commands Executed

### Create Sample Data

```bash
mkdir app-data
echo "This is critical client data." > app-data/data.txt
```

### Create and Edit the Backup Script

```bash
nano backup.sh
```

### Set Permissions and Execute the Script

```bash
chmod +x backup.sh
./backup.sh
```

### Verify the Backup Archive

```bash
ls -l backups/
tar -tzf backups/backup_*.tar.gz
```

### Configure and Verify the Cron Job

```bash
crontab -l
env EDITOR=nano crontab -e
crontab -l
```

The cron expression configured for the daily backup is:

```bash
0 2 * * * /root/backup.sh
```

### Documentation Files

```bash
nano backup-script-guide.md
nano README.md
```

## 4. Skills Learned

- **Bash scripting:** Writing shell commands to automate repetitive tasks.
- **Variables:** Storing directory paths and timestamps for easier script maintenance.
- **Linux permissions:** Using `chmod +x` to make a script executable.
- **File compression:** Using `tar -czf` to create compressed backup archives.
- **Cron scheduling:** Configuring recurring tasks to run automatically.
- **Verification and troubleshooting:** Checking backup files, reviewing cron schedules, and resolving execution errors.
- **Technical documentation:** Writing clear instructions and explanations for an IT team.

## 5. Expected Project Structure

```text
Laboratory-09-Cloud-Automation-Engineer/
├── README.md
├── automation-research.md
├── backup-script-guide.md
├── backup.sh
├── app-data/
│   └── data.txt
├── backups/
│   └── backup_TIMESTAMP.tar.gz
└── screenshots/
    ├── script-execution.png
    └── cron-schedule.png
```

The structure above represents the expected organization. Some files or folders may need to be created or moved into the laboratory directory.

## 6. Conclusion

This laboratory demonstrates how Linux tools can automate backup operations and reduce manual work. The combination of Bash scripting, file permissions, compression, and cron scheduling provides a foundation for understanding cloud operations and routine system maintenance.
