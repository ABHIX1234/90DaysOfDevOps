# Day 07 – Linux File System Hierarchy & Scenario-Based Practice

This day focuses on understanding **where things live in Linux** and how that knowledge helps in **real-world DevOps troubleshooting**.

Instead of memorizing commands, the goal is to learn **how to think and debug like a DevOps engineer**.

---

## 📂 Topics Covered

### 1️⃣ Linux File System Hierarchy

Learned the purpose and usage of important Linux directories such as:

- `/` – Root of the file system
- `/home` – User home directories
- `/root` – Root user’s home directory
- `/etc` – Configuration files
- `/var/log` – System and service logs
- `/tmp` – Temporary files
- `/bin`, `/usr/bin` – Command binaries
- `/opt` – Optional / third-party applications

For each directory:

- Understood what it contains
- Explored files using `ls`
- Noted when and why it is used

---

### 2️⃣ Scenario-Based Troubleshooting

Practiced real DevOps-style scenarios:

- Service not starting after reboot
- High CPU usage on a server
- Finding logs for systemd services
- Fixing file permission issues

Each scenario was solved step-by-step using:

- `systemctl`
- `journalctl`
- `top`, `ps`, `htop`
- `chmod`, `ls -l`

Focus was on **troubleshooting flow**, not just commands.

---

## 🧠 Key Learnings

- Knowing the Linux file system saves time during incidents
- Logs and configs are easier to find with proper structure knowledge
- Scenario-based practice builds confidence for real production issues
- These skills are directly useful for **DevOps interviews and on-call work**

---

## 📁 Files in This Folder

- `day-07-linux-fs-and-scenarios.md` → Detailed notes and scenarios
- `README.md` → Overview of Day 07 learning

---

## 🚀 Part of 90DaysOfDevOps

This work is part of the **90DaysOfDevOps** learning challenge.

Hashtags:
