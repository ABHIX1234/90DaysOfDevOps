# Day 12 - Breather & Revision (Days 01-11)

## Checkpoints

- [x] Mindset and plan reviewed (Day 01)
- [x] Processes/services commands rerun (Day 04/05)
- [x] File skills practiced (Days 06-11)
- [x] Cheat sheet refreshed (Day 03)
- [x] User/group scenario recreated (Day 09/11)

## Review Notes

### Mindset and Plan

- Revisited Day 01 learning plan: goals still aligned with building DevOps fundamentals. Tweaked to include more hands-on practice in the next weeks to reinforce automation and monitoring concepts.
- Key takeaway: consistency matters; set a daily 30-45 minute block.

### Processes and Services

- Reran `ps aux | head -10`: observed system daemons, user shells, and background services. `ps` provides a snapshot of current processes.
- Reran `systemctl status sshd`: service active/running. Checked logs with `journalctl -u sshd --since today`; no errors, service healthy.
- Observation: processes are dynamic; services like SSH are critical for remote access and should be monitored regularly.

### File Skills

- Practiced `echo "test" >> testfile.txt`: appended text to file.
- Practiced `chmod 755 script.sh`: set executable for owner, readable/executable for group and others.
- Practiced `ls -l`: verified permissions and ownership.
- Key ops: these commands are essential for file management; octal `chmod` (e.g., 755) is now clearer.

### Cheat Sheet Refresh

- Skimmed Day 03 commands: top 5 for incidents.
- `ps aux`: quick process overview.
- `systemctl status <service>`: check service health.
- `journalctl -u <service>`: view logs for troubleshooting.
- `ls -l`: inspect file permissions.
- `chmod`: adjust permissions safely.

### User/Group Sanity

- Recreated scenario: created user `testuser` with `sudo useradd testuser`, then changed ownership with `sudo chown testuser:testuser testfile.txt`.
- Verified with `id testuser` (UID/GID) and `ls -l testfile.txt` (ownership shows `testuser`).
- Takeaway: user management is straightforward but requires sudo; always verify changes.

## Mini Self-Check

1. **Which 3 commands save you the most time right now, and why?**
   - `ps aux`: quickly lists processes for monitoring system health.
   - `systemctl status <service>`: checks service status without digging deeper.
   - `ls -l`: provides detailed file info, saving time on permission checks.

2. **How do you check if a service is healthy? List the exact 2-3 commands you would run first.**
   - `systemctl status <service>`: checks if active and running.
   - `journalctl -u <service> --since today`: reviews recent logs for errors.
   - `ps aux | grep <service>`: confirms the process is alive.

3. **How do you safely change ownership and permissions without breaking access? Give one example command.**
   - Use `chmod` with specific permissions and `chown` carefully. Example: `chmod 644 file.txt` to keep owner write access while allowing read for others.

4. **What will you focus on improving in the next 3 days?**
   - Deepen understanding of networking basics (e.g., `netstat`, `ss`).
   - Practice scripting with Bash for automation.
   - Explore containerization with Docker to build on file and process skills.
