# Week 13 Linux Fundamentals - Setup Log & Runbook

- `sudo apt update && sudo apt upgrade -y` | Refreshed local package index and updated system libraries to latest stable versions.
- `sudo apt install -y tree tldr git vim file pipx` | Installed essential DevOps utilities for directory inspection, quick command reference, version control, text editing, binary analysis, and isolated python execution.
- `which tree tldr git vim file pipx` | Verified that all newly installed utility binaries are accessible in the system PATH.
- `mkdir -p ~/week-13-linux/exercises` | Created the central project workspace and exercises subdirectory structure.
- `cd ~/week-13-linux` | Navigated into the main week-13-linux repository directory.
- `git init` | Initialized a local Git repository for version control and runbook tracking.
- `touch setup-log.md README.md` | Created core project documentation and runbook files.
- `sudo apt install -y apache2` | Installed the Apache HTTP web server daemon to handle local web testing.
- `sudo systemctl start apache2` | Started the Apache web server daemon to test local HTTP responsiveness.
- `sudo systemctl status apache2` | Verified that the Apache service is actively running and bound to system ports.

navigating and creating directory tree blind without a file manager.

/home/princewill_onyema/practice:
total 24
drwxr-xr-x 6 princewill_onyema princewill_onyema 4096 Oct 18 00:01 .
drwxr-x--- 9 princewill_onyema princewill_onyema 4096 Oct 18 00:13 ..
drwxr-xr-x 2 princewill_onyema princewill_onyema 4096 Oct 18 00:03 archive
drwxr-xr-x 2 princewill_onyema princewill_onyema 4096 Oct 18 00:03 config
drwxr-xr-x 2 princewill_onyema princewill_onyema 4096 Oct 18 00:02 docs
drwxr-xr-x 2 princewill_onyema princewill_onyema 4096 Oct 18 00:03 scripts

/home/princewill_onyema/practice/archive:
total 8
drwxr-xr-x 2 princewill_onyema princewill_onyema 4096 Oct 18 00:03 .
drwxr-xr-x 6 princewill_onyema princewill_onyema 4096 Oct 18 00:01 ..
-rw-r--r-- 1 princewill_onyema princewill_onyema    0 Oct 18 00:03 old-notes.txt

/home/princewill_onyema/practice/config:
total 8
drwxr-xr-x 2 princewill_onyema princewill_onyema 4096 Oct 18 00:03 .
drwxr-xr-x 6 princewill_onyema princewill_onyema 4096 Oct 18 00:01 ..
-rw-r--r-- 1 princewill_onyema princewill_onyema    0 Oct 18 00:03 settings.conf

/home/princewill_onyema/practice/docs:
total 12
drwxr-xr-x 2 princewill_onyema princewill_onyema 4096 Oct 18 00:02 .
drwxr-xr-x 6 princewill_onyema princewill_onyema 4096 Oct 18 00:01 ..
-rw-r--r-- 1 princewill_onyema princewill_onyema   56 Oct 18 00:02 notes.txt

/home/princewill_onyema/practice/scripts:
total 12
drwxr-xr-x 2 princewill_onyema princewill_onyema 4096 Oct 18 00:03 .
drwxr-xr-x 6 princewill_onyema princewill_onyema 4096 Oct 18 00:01 ..
-rwx------ 1 princewill_onyema princewill_onyema   25 Oct 18 00:03 hello.sh

# Exercise 4: Permissions Drill - Runbook & Log

- `touch public.txt script.sh secret.env shared.txt locked.txt` | Created the five target files for the permissions drill.
- `chmod 644 public.txt` | Set public.txt to owner read/write, everyone read.
- `chmod 755 script.sh` | Set script.sh to owner full control, everyone read/execute.
- `chmod 600 secret.env` | Set secret.env to owner read/write only.
- `chmod 664 shared.txt` | Set shared.txt to owner/group read/write, others read.
- `chmod 400 locked.txt` | Set locked.txt to owner read-only.
- `ls -l public.txt script.sh secret.env shared.txt locked.txt` | Verified numeric permission flags.
- `chmod u=rw,go=r public.txt` | Set public.txt permissions using letter notation.
- `chmod u=rwx,go=rx script.sh` | Set script.sh permissions using letter notation.
- `chmod u=rw,go= secret.env` | Set secret.env permissions using letter notation.
- `chmod ug=rw,o=r shared.txt` | Set shared.txt permissions using letter notation.
- `chmod u=r,go= locked.txt` | Set locked.txt permissions using letter notation.
- `ls -l public.txt script.sh secret.env shared.txt locked.txt` | Confirmed all letter notation permissions match expected flags.
- `mkdir testdir` | Created a test directory for the execute-bit experiment.
- `chmod -x testdir` | Removed the execute permission bit from the directory.
- `cd testdir` | Attempted to traverse into the directory and encountered permission denial.

# Directory Permission Observation & Error Log
- Exact Error: `bash: cd: testdir: Permission denied`
- Explanation: The execute bit (`x`) on a directory controls search and traversal privileges. Removing it prevents the shell from traversing into `testdir` regardless of whether read permissions are active.
