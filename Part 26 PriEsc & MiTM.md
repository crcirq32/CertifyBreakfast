## Privilege Escalation

### Definition
- **Purpose**: Gaining access to resources or permissions beyond what a user is authorized to access.
- **Examples of Access**:
  - Files
  - Database records
  - Network locations

### Methods
- Start as a "normal user" and escalate privileges.
- Inject code into a privileged application.
- Utilize commands like **sudo** or "Run as Administrator."

---

## Mitigation Strategies

- **Password Management**: Use strong, unique passwords.
- **Multi-Factor Authentication (MFA)**: Adds an extra layer of security.
- **Least Privilege Principle**: Limit user permissions to the minimum necessary.
- **Input Validation**: Sanitize user input to prevent injection attacks.
- **Patching**: Regularly update software to fix vulnerabilities.
- **Change Default Credentials**: Remove or change default passwords, which are often publicly accessible.

---

## Pass the Hash Attack

### Definition
- **Technique**: Presenting the hash value of a password instead of the password itself.
  
### Vulnerabilities
- Older versions of Windows that use LM hashes.
- Newer versions configured for backward compatibility.

### Golden Ticket
- **Description**: An identifier that can grant any permission in an Active Directory domain.
- **Mechanism**: Uses Kerberos to grant administrative permissions.

---

## Man-in-the-Middle (MitM) Attack

### Definition
- **Networking Aspect**: Interception of network traffic by a third party.
- **Software Aspect**: Code injection into an application to intercept user actions (e.g., Man-in-the-Browser, MitB).

### Keyloggers
- Malicious programs that run invisibly on a device, capturing keystrokes.

### Example: ARP Poisoning
- **Overview**: An old protocol that can be manipulated due to its trusting nature.
- **Impact**: Allows alteration of MAC addresses.

#### Mitigation
- **Dynamic ARP Inspection (DAI)**: Configured on switches to verify ARP requests/responses.
  - **Legitimacy Check**: Uses DHCP Snooping to validate legitimate IP addresses.

---

## DNS Attacks

### Overview
- **Function of DNS**: Resolves website names to their corresponding IP addresses.

### Types of Attacks
1. **Buffer Overflows**: Can modify, crash, or read information from web servers.
2. **DNS Amplification**: A small request generates a disproportionately large response, akin to a DoS attack.

### Mitigation Strategies
- **Patching**: Update DNS software to address vulnerabilities.
- **Traffic Filtering**: Block malicious sources and filter undesirable traffic.

---

## Rootkits

### Definition
- A type of kernel-level malware that infects or replaces operating system files with malicious ones.
  
### Requirements
- Requires root-level (administrator) access for installation.
- Commonly infects DLL files in Windows environments.

### Mitigation Strategies
- **Antivirus Software**: Detects and removes malicious code.
- **File Integrity Monitoring (FIM)**: Monitors OS files for unauthorized changes.
  - **Hashing**: Use hashing to detect changes in file content; any alteration indicates tampering.

### Tripwire
- **Description**: A leading example of file integrity monitoring.
- **Functionality**:
  - Monitors file changes using a local database, tracking hashes, timestamps, and file ownership.

#### Alternative
- **FileSight**: Another solution for file integrity monitoring.

---