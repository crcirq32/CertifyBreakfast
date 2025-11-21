## Host-Based IoCs

### 1. Malicious Processes

- **Definition**: Identifying active malicious processes running on the host.
- **Indicators**:
  - Process baseline.
  - Scanning for malicious code in running processes.
  - Monitoring unexpected registry changes.
  - Observing open files and network traffic.
  
- **Tools for Monitoring**:
  - **Windows**: Task Manager, Process Explorer.
  - **Linux**: `ps` command, `top`, or `htop` commands.
  - **MacOS**: Activity Monitor.

---

### 2. High Resource Usage IoCs

- **Definition**: Understanding what constitutes "high" resource usage.
- **Indicators**:
  - Establishing a baseline will aid in determining normal usage.
  - Elevated resource usage is not always indicative of malicious activity.

---

### 3. Disk and Malware IoCs

#### Exfiltration IoCs

- **Indicators**:
  - Writing to temporary folders.
  - Masking data as log files.
  - Archiving or encrypting collected data.
  - Utilizing NTFS or Recycle Bin for storage.
  - Data staging practices.

#### File System Analysis

- **Indicators**:
  - Timestamps and last modification dates.
  - File ownership and access control lists.

#### Disk Space Usage IoCs

- **Definition**: Malicious software can excessively consume disk space, often for storing files.
- **Tools for Identification**:
  - **Windows**: Total Commander.
  - **Linux/MacOS**: `du` command for disk usage.

#### File Handles IoCs

- **Indicators**: High volume writes and unusual file activity.

---

### 4. Unauthorized Privilege IoCs

- **Indicators**:
  - Privilege escalation attempts.
  - Unauthorized sessions and failed login attempts (potential brute-force attempts).
  - Creation of new user accounts or suspicious activities from guest accounts.
  - Monitoring privilege usage outside of normal working hours.
  - Changes in security policies.

---

### 5. Unauthorized Software IoCs

- **Indicators**:
  - Presence of unknown software or unexpected security tools.
  - Reviewing prefetch files, Cisco AMP, and cache data can aid in detection.

---

### 6. Unauthorized Changes and Hardware IoCs

- **Indicators**:
  - System configuration changes (e.g., security setting modifications).
  - Unapproved hardware peripherals, such as USB drives that may contain malicious firmware.

---

### 7. Persistence IoCs

- **Definition**: Mechanisms by which malware can survive reboots or user log-offs.
- **Indicators**:
  - Modifications in the Windows registry.
  - Running applications set to auto-start via the registry (`Run`, `RunOnce`).
  - Scheduled tasks for automated runs.
  
---

### 8. Application-Based IoCs

- **Indicators**:
  - Network connections, including strange port numbers and outbound connections indicative of malware communicating with a command-and-control (C2) server.
  - Anomalies in application logs, such as code injection or directory traversal attempts.
  - Service defacement events and service interruptions.

**Monitoring Tools**:
  - **Windows**: `netstat`, `Get-Service` (PowerShell).
  - **Linux**: Daemons are monitored using `ps`, `top`, or `systemctl`.

---

### 9. Application Logs IoCs

- **Importance**: Logs can provide critical insights.
- **Key Monitoring Areas**:
  - DNS queries and accessed destinations for anomalies.
  - Web server logs for HTTP status codes (4xx client errors, 5xx server errors).
  - FTP logs capturing all connections and commands.
  - SQL access logs for execution status and queries.

---

### 10. New Account IoCs

- **Indicators**:
  - Creation of new user accounts, especially rogue accounts.
  - Monitoring local vs. Active Directory accounts.
  
**Tools for Detection**:
  - **Windows**: Local account checking.
  - **Linux**: 
    - `w` command for current users.
    - `lastlog` for login history.
    - Viewing `/var/log/auth.log` for account creation commands.
    - `faillog` for tracking authentication failures.

---

### 11. Virtualized App IoCs

- **Indicators**:
  - Process and memory analysis using hypervisor VM introspection tools.
  - Analysis of VM disk files, including recovery of deleted files.
  - Configuration changes in system logs.

---

### 12. Mobile App IoCs

- **Challenges**: Difficult to identify due to limited visibility.
- **Indicators**:
  - Bypassed phone security measures and default device settings.
  - Monitoring cloud data, including backups, login data, and session data.
  - Analyzing carrier data for geolocation tracking.

