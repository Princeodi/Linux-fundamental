# Exercise 6 & 7: Log Navigation, Permissions, and System Break-Fix Runbook

- **Log Exploration & Inspection**: Navigated to `/var/log`, inspected system journals, and monitored live event streaming using `tail -f syslog`.
- **Fault Introduced**: Stripped permissions on `02-bandit.md`, removed execute permissions from the `practice` directory (`chmod -x`), and created a restricted root-owned file via `sudo touch /tmp/roots-file`.
- **Diagnosis**: Encountered `-bash: cd: practice: Permission denied` when attempting to traverse the locked directory, along with permission errors during unauthorized edits or timestamp modifications.
- **fixing**: Restored proper file permissions (`chmod 644`), re-enabled directory traversal (`chmod +x practice`), and managed root-level files using elevated privileges.
- **Verification**: Confirmed successful recovery and operational status of files and directories using `ls -la`.
