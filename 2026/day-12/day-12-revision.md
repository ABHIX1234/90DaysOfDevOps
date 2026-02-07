# Day 12 – Breather & Revision (Days 01–11)

## Review Notes

### Mindset & Plan

- Revisited Day 01 learning plan: Goals are still aligned with building DevOps fundamentals. Tweaked to include more hands-on practice in the next weeks to reinforce concepts like automation and monitoring.
- Key takeaway: Consistency in daily learning is crucial; adjusted schedule to allocate 30-45 minutes daily without fail.

### Processes & Services

- Reran `ps aux | head -10`: Observed running processes including system daemons, user shells, and background services. Noted that `ps` provides a snapshot of current processes.
- Reran `systemctl status sshd`: Service is active and running. Checked logs with `journalctl -u sshd --since today` – no errors, service healthy.
- Observation: Processes are dynamic; services like SSH are critical for remote access and should be monitored regularly.

### File Skills

- Practiced `echo "test" >> testfile.txt`: Appended text to file successfully.
- Practiced `chmod 755 script.sh`: Changed permissions to executable for owner, readable for group and others.
- Practiced `ls -l`: Verified permissions and ownership of files in directory.
- Key ops: These commands are essential for file management; `chmod` with octal notation (e.g., 755) is now clearer.

### Cheat Sheet Refresh

- Skimmed Day 03 commands: Highlighted top 5 for incidents:
  1. `ps aux`: Quick process overview.
  2. `systemctl status <service>`: Check service health.
  3. `journalctl -u <service>`: View logs for troubleshooting.
  4. `ls -l`: Inspect file permissions.
  5. `chmod`: Adjust permissions securely.

### User/Group Sanity

- Recreated scenario: Created a new user `testuser` with `sudo useradd testuser`, then changed ownership of a file with `sudo chown testuser:testuser testfile.txt`.
- Verified with `id testuser` (shows UID/GID) and `ls -l testfile.txt` (shows ownership as testuser).
- Takeaway: User management is straightforward but requires sudo; always verify changes.

## Mini Self-Check

1. **Which 3 commands save you the most time right now, and why?**
   - `ps aux`: Quickly lists all processes for monitoring system health.
   - `systemctl status <service>`: Instantly checks if a service is running without digging deeper.
   - `ls -l`: Provides detailed file info, saving time on permission checks.

2. **How do you check if a service is healthy? List the exact 2–3 commands you’d run first.**
   - `systemctl status <service>`: Checks if active and running.
   - `journalctl -u <service> --since today`: Reviews recent logs for errors.
   - `ps aux | grep <service>`: Confirms the process is alive.

3. **How do you safely change ownership and permissions without breaking access? Give one example command.**
   - Use `chmod` with specific permissions and `chown` carefully. Example: `chmod 644 file.txt` (read/write for owner, read for others) to maintain access while securing.

4. **What will you focus on improving in the next 3 days?**
   - Deepen understanding of networking basics (e.g., `netstat`, `ss` commands).
   - Practice scripting with Bash for automation.
   - Explore containerization with Docker to build on file and process skills.
