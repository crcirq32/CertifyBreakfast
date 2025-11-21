## Network-Based IoCs

### 1. Network DoS Attacks

- **Definition**: Exhausts bandwidth or connection resources on a server, potentially bringing down the network or service.
- **Indicators**:
  - Bandwidth consumption spikes.
  - Spikes in traffic.
- **Detection**: 
  - Utilize monitoring and alerting systems.
  - Establishing a baseline is beneficial for identifying anomalies.

---

### 2. Distributed Denial of Service (DDoS)

- **Description**: An attacker uses a botnet to control many machines that send synthetic traffic to overwhelm a network.
- **Mitigation**: 
  - Redirect traffic into a sinkhole or blackhole to prevent it from reaching your network.

### 3. Distributed Reflected Denial of Service (DRDoS)

- **Mechanism**: Spoofs the victim's IP address and sends requests to servers that generate large responses.
- **Protocols Suited for This Attack**:
  - HTTP
  - DNS
  - NTP
- **Example**: **Slashdotting** – posting a link to a website on social platforms (e.g., Reddit) leading to sudden, excessive traffic.

---

### 4. Beaconing

- **Definition**: Regular signaling, resembling a heartbeat, that might use low amounts of network traffic (e.g., SYN packets).
- **Indicators**:
  - Changing IPs and domains.
  - Protocols used:
    - IRC (Internet Relay Chat)
    - HTTP(S) (HTTP Secure)
    - DNS
    - Social media postings (e.g., Facebook, LinkedIn, Twitter)
    - Cloud services and media files.

---

### 5. P2P IoCs

- **Traffic**: Typically unwanted traffic occurring within the same network.
- **Execution**: Common with worms or hidden in protocols such as:
  - SMB (Server Message Block) – file sharing protocol.
  - IPP (Internet Printing Protocol) – used for printer connections.
- **ARP Usage**: Employed to resolve IP addresses to MAC addresses and can be a vector for Man-in-the-Middle (MitM) attacks.

---

### 6. Rogue Devices

- **Characteristics**:
  - Unaccounted for or unwanted devices connected to the network.
- **Detection Methods**:
  - Network mapping.
  - Visual inspections.
  - Wireless monitoring for interference.
  - Traffic sniffing to analyze protocol types.
  - Network Access Control (NAC) and intrusion detection.
  - IP address management to track allocated addresses.

---

### 7. Network Scan and Sweep Events

- **Sweeping**: Identifies which hosts are up in a network.
- **Fingerprinting**: Conducts deeper port scans on hosts to reveal:
  - Running services, software, operating systems, and installed patch levels.
  
- **Detection**: Identified by Intrusion Detection Systems (IDS) and Intrusion Prevention Systems (IPS) using known patterns.

---

### 8. Non-Standard Port Usage IoCs

- **Port Ranges**:
  - **Well-Known Ports**: 0-1023 TCP/UDP.
  - **Registered Ports**: 1024-49151 TCP/UDP.
  - **Dynamic and Private Ports**: 49152-65535 TCP/UDP (assigned by IANA).
  
- **Indicators**: Mismatched ports and applications.
- **Tools for Detection**:
  - **Netcat**: Detect SSH reverse shells.
  - **Cryptcat**.
  - **Pupy**.

---

### 9. Data Exfiltration IoCs

- **Channels**: 
  - HTTP(S) (public storage services like Dropbox, OneDrive, Google Drive).
  - Web application attacks (e.g., SQL injection).
  - DNS as a covert channel (e.g., using TXT records for encrypted communication).
  - Instant Messaging, P2P, Email, FTP.
  - Encrypted tunnels (VPNs, IPSec, SSL).

---

### 10. Overt vs. Covert Channels IoCs

- **Overt Channels**: Easily observable and in plain sight.
- **Covert Channels**: Stealthy and designed to avoid detection.
  - **Techniques**:
    - Outbound traffic is seldom filtered.
    - Encoding data in protocol headers.
    - Packet fragmentation.
    - Encryption methods.
    - Steganography: hiding information within images or videos.
    - Storage and timing channels.