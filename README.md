Linux Systems Engineering Runbook

Welcome to my centralized engineering runbook and exercise repository for Linux fundamentals. This documentation covers hands-on command-line exercises, permission drills, system diagnostics, log inspection, and break-fix recovery scenarios executed within an Ubuntu 24.04 WSL2 environment.

🛠️ Environment & Tooling
- **Operating System**: Ubuntu 24.04 (WSL2)
- **Core Utilities**: `chmod`, `systemctl`, `journalctl`, `du`, `df`, `free`, `ps`, `vim`, `grep`, `tail`


📁 Repository Structure & Exercises

Permissions Drill (`exercises/04-permissions.md`)
- **Focus**: Mastering file and directory access control using numeric and symbolic notation.
- **Key Actions**: 
  - Applied precise permissions (`644`, `755`, `600`, `400`) to various file types.
  - Tested directory traversal constraints by stripping and restoring the execute bit (`chmod -x` / `chmod +x`).

Explain Before You Run (`exercises/05-explain.md`)
- **Focus**: Understanding system resource inspection and performance monitoring utilities.
- **Key Actions**: Documented expected vs. actual behaviors for critical hardware and process diagnostic commands (`ls -lath`, `du -sh`, `df -h`, `free -h`, `uname -a`, `uptime`, `ps aux`).

Find the Log (`exercises/06-logs.md`)
- **Focus**: Locating, navigating, and inspecting system-level and application log files.
- **Key Actions**: 
  - Explored centralized logs under `/var/log/`.
  - Queried system authentication events via systemd journals (`journalctl`).
  - Streamed live system events in real-time using `tail -f` paired with package manager updates (`sudo apt update`).

Break It and Fix It (`exercises/07-break.md`)
- **Focus**: Developing SRE resilience by deliberately introducing faults and executing professional remediation.
- **Key Actions**:
  - **File Lockout**: Stripped file permissions (`chmod 000`) and successfully recovered access.
  - **Traversal Lockout**: Removed directory execute permissions to simulate `Permission denied` traversal errors and restored access.
  - **Root-Owned Files**: Handled permissions and modifications for files created with elevated `sudo` privileges.

🚀 Execution & Verification
All exercises have been systematically tested, documented, and committed to track progressive administrative proficiency in Linux environments.
