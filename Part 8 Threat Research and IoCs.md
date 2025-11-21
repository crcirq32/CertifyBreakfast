## Signature-Based Detection

- **Definition**: Helps to recognize malware.
- **Advantages**: 
  - Efficient and easy to update.
- **Detection Mechanisms**: 
  - Byte patterns.
  - Analyzing files, processes, and packets.
- **Challenges**:
  - Becomes tougher with encrypted data.

---

## Attacker Strategies to Avoid Detection

- **Signature Evasion**:
  - Create malware with no recognizable signature.
- **Complexity**:
  - Develop complex malware that requires context and multiple signatures, making it behave like legitimate applications.

---

## Malware Detection Without Signatures

### Indicators of Compromise (IoCs)

- **Definition**: Indications left behind that show evidence of compromise.
- **Key Behaviors to Monitor**:
  - Abnormal URLs.
  - New files.
  - Files executed in unusual scenarios.
  - Suspicious processes found in memory.
  - Remote Access Tools (RAT) controlling machines.
  - Unusual file hashes associated with bad reputations.
  - New registry entries.
  - Excessive resource usage (CPU, memory, disk).
  - New applications detected using `netstat`.
  - Anomalous network protocols.
  - New devices on the network.
  - Signs of data exfiltration.

### Perspectives on IoCs

- Shifts in the understanding of IoCs can adapt detection methods effectively.

### Automated Tools

- **Host-based Intrusion Prevention System (HIPS)**.
- **Host-based Intrusion Detection System (HIDS)**.
- **Endpoint security suites**.

### Correlation Tools

- **Security Information and Event Management (SIEM)** solutions.

---

## Determining Good vs. Bad Indicators

### Reputational Methods

- Associate IoCs with reputation data (e.g., URLs, hashes, IP addresses, email layouts).
- Assess historical associations with attacks.
- Use databases and online subscriptions (e.g., Cisco Talos).

### Behavioral Methods

- Analyze actions of potential threats:
  - For example, `Calculator.exe` attempting internet connections.
  - Unusual file alterations (e.g., multiple files changed simultaneously).
  - Changes in user settings.

- **Baseline Importance**: Establishing a baseline of normal behavior allows easy detection of unexpected actions.

---

## Attack Patterns

### Tactics, Techniques, and Procedures (TTP)

- **Denial of Service (DDoS)**: Detect unexpected high traffic or random connections.
- **Malware Indicators**: Look for high CPU, memory, and disk activity.
- **Reconnaissance**: Monitor half-open ports, short-lived connections, and patterns of simultaneous connections across ports.
- **Advanced Persistent Threats (APTs)**:
  - Identify remote control traffic.
  - Monitor for port hopping, fast flux DNS changes, and data exfiltration alerts.
  - Watch for anomalies in protocol definitions (e.g., unusually high payloads).

---

## Threat Modeling

### STIX (Structured Threat Information eXpression)

- **Versions**:
  - Version 2: JSON format.
  - Version 1: XML format.
- **Components**:
  - SDOS (STIX Domain Objects).
    - Observed data (e.g., IP addresses, file properties).
    - Indicators of threats.
    - TTP documentation.
    - Campaigns and threat actors.
    - Recommended courses of action.

### TAXII (Trusted Automated Exchange of Intelligence Information)

- **Functionality**: Protocol for transporting STIX data.
- **API Methods**: Uses RESTful API operations to enable data transfers.
- **Data Transport Types**:
  - **Collections**: Basic interfaces to threat information databases.
  - **Channels**: Data pushed to clients via feeds, with subscriptions for automatic updates.
    - Examples of sources:
      - Open IOC
      - FireEye
      - MISP
      - X-Force Exchange

---