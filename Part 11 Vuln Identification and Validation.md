## Vulnerability Identification

### What to Scan?

#### Asset Criticality

- **Purpose**: Prioritize what to monitor and fix based on asset importance. 
- **Types of Assets**:
  - **People**: Employees, partners, suppliers, etc.
  - **Tangible Assets**: Equipment, buildings, etc.
  - **Intangible Assets**: Product ideas, brand reputation.

#### Asset and Inventory Tracking

- **Strategy**: Track assets with a dedicated tool that maintains:
  - Type, model, serial number (SN), ID, location, user, value, service information.
- **Classification Examples**:
  - Usage
  - Networks
  - Sensitivity
  - Outside connections
  - Financial values
  - Legal requirements
  - Contractual obligations

---

### Infrastructure Vulnerability Scanners

- **Definition**: Different from basic tools like Nmap, focusing on comprehensive vulnerability assessment.
- **Capabilities**:
  - Scans hosts and network devices.
  - Identifies vulnerabilities in:
    - OS versions and patches
    - Running services
    - Configuration settings
    - Network shares
    - User accounts
    - Weak security policies

---

### Initial Steps of a Vulnerability Scanner

#### Mapping and Enumeration

- **Inventory tasks**: Devices, versions, plugins, etc.
  
##### Scanning Types

1. **Passive Scanning**:
   - Detects public information and captures network traffic.
   - **Characteristics**:
     - Zero interaction with target.
     - Minimal impact on network.
     - Limited detail and mostly undetectable.

2. **Active Scanning**:
   - Interacts directly with the target to elicit responses.
   - **Characteristics**:
     - Conducted during non-working hours.
     - Can create performance issues and easily detected.

---

### Scanning Methods

1. **Credentialed Scan**:
   - Utilizes admin or user accounts.
   - Provides the highest level of detail from an insider's perspective.
  
2. **Non-Credentialed Scan**:
   - Useful for network scoping but requires more bandwidth.
   - No user account; offers an outside viewpoint.
   - Best for perimeter scanning but higher risk of inaccurate results and downtime.

3. **Server-Based Scanning**:
   - Connects to servers for credentialed or non-credentialed scans.

4. **Agent-Based Scanning**:
   - Involves a plugin or application installed on hosts.
   - **Advantages**:
     - Always credentialed by default.
     - Efficient with low bandwidth consumption.
     - Works with offline devices (mobile, laptops).
   - **Disadvantages**:
     - Increased management overhead.
     - Potential vulnerability as an attack vector.

5. **Segmentation**:
   - Scanners must connect to assets adequately.
   - Ensure reachability through subnets, VLANs, and VPNs.
   - Consider using a dedicated management network (separate VLAN or physical network).

---

### Frequency of Scanning

- **Determining Factors**:
  - Risk appetite.
  - Technical constraints (service degradation, time limits, licensing).
  
- **Recommended Scanning Times**:
  - When system changes occur.
  - As mandated by regulations.
  - After a security breach.

---

### Choosing a Scanner

- **Types**:
  - **Free Tools**.
  - **Paid Tools**: Generally rely on proprietary databases of vulnerabilities; often updated and maintained.
  - **Specialized Scanners**:
    - Web app scanners for finding vulnerabilities in web applications.
    - Mobile app scanners.
    - Network scanners to assess network weaknesses.

#### Example Scanners

- **NESSUS**:
  - Well-known for both free and paid versions.
  - Offers built-in scanning profiles and allows custom profiles using NASL (Nessus Attack Scripting Language).
  
- **OPENVAS**:
  - Developed from NESSUS codebase.
  - Open-source and part of the Greenbone Security Assistant community.
  
- **Qualys**:
  - Cloud-based service.
  - Utilizes sensors distributed throughout the network, including cloud locations.