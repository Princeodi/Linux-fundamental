06-logs.md
# Exercise 6: Find the Log — Runbook

1. **Which log file is largest?**
   - **Command**: `sudo du -h --max-depth=1 /var/log | sort -hr`
   - **Answer**: 322K Oct 17 00:20 dpkg.log.1.

2. **What was the most recent authentication event?**
   - **Command**: `sudo journalctl -u ssh -n 5 --no-pager`
   - **Answer**: Retrieved the latest SSH connection handshakes and authentication attempts(sudo apt update on second session).

3. **Run tail -f on a log, then run sudo apt update. What appeared?**
   - **Command**: `sudo tail -f /var/log/syslog` paired with `sudo apt update` in a separate terminal window.
   - **Answer**: Real-time log streams appeared detailing package manager databases.

