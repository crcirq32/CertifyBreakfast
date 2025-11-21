## Attack Framework

- **Definition**: A standardized way of describing what occurs before, during, and after an attack.
- **Key Questions Addressed**:
  - Who is the attacker?
  - What resources are being attacked?
  - How is the attack being conducted?
- **Purpose**: Aids in threat modeling.

---

## The Cyber Kill Chain

- **Overview**: Defines attack phases and is mainly related to Advanced Persistent Threats (APTs).
- **Key Components**:
  - Indicators of Compromise (IoCs).
  - Tactics, Techniques, and Procedures (TTPs).
  - Mitigation methods.

### Phases of the Cyber Kill Chain

1. **Reconnaissance**:
   - The attacker gathers information stealthily about defenses, business processes, and personnel.
  
2. **Weaponization**:
   - Exploitation of weaknesses identified during reconnaissance to develop tools for the attack.
  
3. **Delivery**:
   - Methods for exploiting weaknesses and delivering malicious code (e.g., via email, USB, web).
  
4. **Exploitation**:
   - Gaining access to the system through automated or manual means.

5. **Installation**:
   - Installing malware on the asset, including backdoors.

6. **Command and Control (C2)**:
   - Establishing a data channel for remote control.
   - Malware communicates back to the attacker's server.

7. **Actions on Objectives**:
   - Attacker accomplishes goals with persistent access.

### Drawbacks of the Cyber Kill Chain

- Primarily focuses on outside threats, neglecting insider threats and cloud environments.
- Difficulty in determining which phase the attacker is in if they erase tracks.
- The model may be oversimplified.

---

## Defense Strategies

### Main Purpose: Installation of Security Controls

- **Defense Strategies for Each Phase**:
  
1. **Reconnaissance**:
   - Reduce the attack surface.
   - Limit information sharing.
   - Educate users.
  
2. **Weaponization**:
   - Regular updates, patches, and fixes.
   - Installation of technical controls.
  
3. **Delivery**:
   - Restrict mass storage usage.
   - Provide user training.
  
4. **Exploitation**:
   - Update, patch, and fix vulnerabilities.
   - Disable unnecessary services to minimize the attack surface.
  
5. **Installation**:
   - Use endpoint security tools to detect abnormal activities and processes.
   - Promote user awareness to recognize potential threats.
  
6. **Command and Control (C2)**:
   - Scan for or filter outbound connections.
  
7. **Actions on Objectives**:
   - If the attacker reaches this stage, it may be too late.
   - Implement tools like Access Control Systems (ACS), Data Loss Prevention (DLP), and offsite backups to mitigate damage.

---

## MITRE ATT&CK Framework

- **Definition**: A comprehensive database of known TTPs mapped to a vast array of attacks.
- **Purpose**:
  - Analyze attacks and determine relevance to specific cases.
  - Aid in mitigating or mitigating against attacks.
- **Significance**: A thorough collection of information on cyber-attacks based on real observations.

---

## Diamond Model of Intrusion Analysis

- **Focus**: Analyzes a single intrusion event by describing relationships between four core features:
  - Adversary
  - Capabilities
  - Victim
  - Infrastructure
- **Characteristics**:
  - Considered oversimplified with based assumptions.
  - Each event has meta features assigned a confidence level.
  - Describes activity threats during an attack across multiple phases.
  
- **Functionality**: Designed for automatic processing, suitable for machines and applications (e.g., ThreatConnect app from Splunk).

---