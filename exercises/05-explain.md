# Exercise 5: Explain Before You Run - Runbook & Log

## 1. ls -lath
- **Prediction**: Lists all files and directories (including hidden ones via `-a`) in long format (`-l`), with human-readable file sizes (`-h`), sorted by modification time (`-t`) with the newest items at the top.
- **Actual Output**: Displayed a detailed list of directory contents ordered chronologically from newest to oldest modification time.
- **Comparison / Difference**: listing files/ not detailed enough

## 2. du -sh *
- **Prediction**: Calculates disk usage (`du`) in a summary total (`-s`) with human-readable units (`-h`) for every file and folder (`*`) in the current directory.
- **Actual Output**: Printed individual size summaries (e.g., `4.0K`, `12M`) for each item in the working directory.

## 3. df -h
- **Prediction**: Reports file system disk space usage (`df`) across all mounted partitions in human-readable sizes (`-h`).
- **Actual Output**: Displayed a table showing filesystems, total sizes, used space, available space, percentage use, and mount points (including WSL virtual drives).

## 4. free -h
- **Prediction**: Displays system memory and swap usage statistics (`free`) formatted with human-readable units (`-h`).
- **Actual Output**: Showed total, used, free, shared, buffer/cache, and available RAM alongside swap memory.

## 5. uname -a
- **Prediction**: Prints all (`-a`) system and kernel information (`uname`), including OS name, kernel release version, build date, and machine hardware architecture.
- **Actual Output**: Outputted Linux kernel details and x86_64 architecture specs for the Ubuntu WSL environment.

## 6. whoami
- **Prediction**: Prints the username of the currently logged-in user account.
- **Actual Output**: Outputted the active username (e.g., `princewill_onyema`).
- **Comparison / Difference**: Matched prediction.

## 7. id
- **Prediction**: Displays the real and effective user ID (UID), group ID (GID), and supplementary group memberships for the current user.
- **Actual Output**: Outputted `uid=1000(...) gid=1000(...) groups=...`.

## 8. uptime
- **Prediction**: Shows how long the system has been running, the current time, the number of logged-in users, and system load averages.
- **Actual Output**: Displayed current time, active uptime duration, 1/5/15-minute load averages.

## 9. history | tail -20
- **Prediction**: Retrieves the command history list and pipes (`|`) the output into `tail -20` to display only the 20 most recent commands executed in the shell session.
- **Actual Output**: Printed a numbered list of the last 20 commands run in the terminal session.

## 10. ps aux
- **Prediction**: Reports a snapshot of active processes (`ps`) across all users (`a`), displaying process owners (`u`) and background/system daemons without a controlling terminal (`x`).
- **Actual Output**: Outputted a comprehensive process table showing PID, CPU/MEM usage, start time, command names, and system services.

