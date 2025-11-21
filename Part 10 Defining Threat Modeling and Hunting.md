## Threat Modeling Questions

- **Key Considerations**:
  - What systems support your business?
  - What is valuable to you?
  - How can these systems be threatened based on the CIA triad (Confidentiality, Integrity, Availability)?

### Important Questions for Threat Modeling

- How would an attack manifest?
- What is the risk of losing Confidentiality, Integrity, or Availability?
- How likely is a specific threat?
- What defenses are currently in place? What is our security posture?
- What security gaps exist? Where are we lacking?

---

## Threat Model Overview

### Adversary Capabilities

- **Definition**: Ability to develop and execute attacks.
  
#### Determining Adversary Capabilities

- Who are the most likely attackers?
- How well-funded are they?

- **Classification of Adversary Capabilities** (MITRE):
  - **Acquired**: Utilizes commodity malware; limited reliance on social engineering.
  - **Augmented**: More experienced; uses known vulnerabilities and custom malware; minimal human involvement.
  - **Developed**: Can create their own malware and delivery methods; may rely on human activity.
  - **Advanced**: Influences attacks with commercial and military assets; wide range of tactics.
  - **Integrated**: Extremely skilled with extensive resources; leverage political assets.

#### Note on Attackers

- **Silver Lining**: Lower-level attackers often avoid overly complex efforts.

---

## Total Attack Surface

- **Definition**: Represents what you own and can potentially be attacked.

### Steps to Determine Your Attack Surface

1. **Inventory**: Identify all physical and non-physical assets.
   - **Devices**: Hardware, sensors, IoT devices.
   - **Applications**: Software in use.
   - **Services**: Cloud services, third-party providers.
   - **Business Processes**: Critical operations.
   - **Corporate Network**:  
     - Wireless networks.
     - Cloud presence.
     - Online presence.
     - Internal applications.
   - **Buildings and People**: Physical security.

- **Strategy**: Aim for a minimal attack surface; harden defenses as much as possible.

---

## Attack Vectors

- **Definition**: Methods of attack on an attack surface.
  
### Types of Attack Vectors

- **Cyber**: Use of malware via systems, social media, emails, USB drives, open ports.
- **Physical**: Exploitation of doors, locks, access cards, and surveillance.
- **Human**: Techniques like impersonation, phishing, coercion, and blackmail.

*Note: These can be combined in a multifaceted attack.*

---

## Likelihood of an Attack

- **Assessment**: How likely is it that an attack will occur?
  - Is it real or probable?
  - Have attacks occurred previously to you or others in your industry?
  - Approach this as an educated guess.

---

## Final Additional Threat Modeling Questions

- What motivates an attack?
- How do other companies defend themselves?
- How frequent are attacks in your industry? This helps acknowledge the likelihood of becoming a victim.

---

## Cyber Threat Hunting

- **Definition**: The proactive search for cyber threats that may otherwise remain undetected.
  
### Key Characteristics

- Requires skills, patience, creativity, and a keen eye for spotting anomalies in systems and networks (i.e., malware).
- Focused on proactive actions rather than waiting for a breach; distinct from incident response.

### Methodology of Threat Hunting

1. Begin from scratch.
2. Establish a hypothesis.
3. Profile potential threat actors.
4. Look for Indicators of Compromise (IoCs) to start the actual hunting process:
   - These may already exist on your devices.
   - Utilize alert systems for investigation.

### Justifying Threat Hunting

- Assess if you have been compromised.
- Discover new attack surfaces.
- Improve threat detection capabilities.
- Provide additional security intelligence.
- Identify critical assets.

