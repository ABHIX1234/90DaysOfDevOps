# 📘 Day 19 – Shell Scripting Project: Log Rotation, Backup & Crontab

## 📌 Overview

Today I applied everything from Day 16–18 into real-world mini projects:

- ✅ Log Rotation Script
- ✅ Server Backup Script
- ✅ Cron Scheduling
- ✅ Maintenance Automation

This day focused on writing production-style automation scripts used in real DevOps environments.

---

# 1️⃣ Log Rotation Script

## 🎯 Objective

- Compress `.log` files older than 7 days
- Delete `.gz` files older than 30 days
- Count compressed and deleted files
- Handle errors safely using strict mode

## 🛠 Key Concepts Used

- `set -euo pipefail`
- `find` with `-mtime`
- `gzip`
- Safe file handling using `-print0`
- Loop with `while read`

## ▶ Example Usage

```bash
./log_rotate.sh /var/log/myapp
```

---

# 2️⃣ Backup Script

## 🎯 Objective

- Create compressed `.tar.gz` backup
- Add timestamp to filename
- Verify archive creation
- Delete backups older than 14 days

## 🛠 Key Commands Used

- `tar -czf`
- `date`
- `find -delete`
- Directory validation
- Argument validation

## ▶ Example Usage

```bash
./backup.sh /home/ubuntu/data /home/ubuntu/backups
```

---

# 3️⃣ Maintenance Automation Script

## 🎯 Objective

- Combine log rotation + backup
- Centralized logging
- Error handling with `trap`
- Production-style structured logging

## 🛠 Concepts Used

- Logging function
- `trap` for error handling
- Redirecting output `>> logfile 2>&1`
- Automation orchestration

---

# 4️⃣ Cron Scheduling

## 🕒 Automate Script Execution

Open crontab:

```bash
crontab -e
```

Example (Run daily at 2 AM):

```
0 2 * * * /home/ubuntu/maintenance.sh
```

## 📖 Cron Format

```
* * * * *
| | | | |
| | | | └── Day of Week (0–7)
| | | └──── Month
| | └────── Day of Month
| └──────── Hour
└────────── Minute
```

---

# 🧠 Key Learning Outcomes

- Writing production-ready shell scripts
- Defensive scripting using strict mode
- Safe file handling
- Backup automation
- Log management
- Cron job scheduling
- Centralized logging
- Error trapping

---

# 🚀 Real-World DevOps Application

These scripts simulate:

- Server maintenance tasks
- Log management
- Backup rotation policies
- Automated daily operations

In production environments, similar logic is handled using:

- `logrotate`
- Cron jobs
- Monitoring tools
- CI/CD automation

---

# 🏆 Final Reflection

Day 19 helped me move from writing individual scripts to building a complete automation workflow combining:

- Log Rotation
- Backup Management
- Error Handling
- Scheduled Execution

This mirrors real-world DevOps operational tasks.

---

# 🔥 Next Goals

- Add email notification on failure
- Upload backups to AWS S3
- Add disk space monitoring
- Add lock mechanism to prevent duplicate runs
- Convert into a structured GitHub project repository
