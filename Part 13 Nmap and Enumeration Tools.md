## Vulnerability Identification

### 1st Step in Vulnerability Process

- **Action**: List all systems in your network.

---

## Enumeration Methods

### Active Enumeration

- **Characteristics**:
  - Makes noise and interacts with targets.
  
- **Categories**:
  - **Footprinting**: Discovering the layout of the network.
  - **Fingerprinting**: Identifying what services are running on a specific host.

### Semi-Passive Enumeration

- **Characteristics**:
  - Mimics normal traffic—"low and slow," "sparse."
  - Low scan profile.

### Passive Enumeration

- **Characteristics**:
  - Makes no noise and listens to network traffic.

---

## Nmap: Network and Host Scanning

- **Overview**: Tool for enumeration and scanning (available at nmap.org).

### Scan Techniques

1. **Ping Scan** (`nmap -sn`):
   - Performs a ping sweep without port scanning.
   - Determines active IP addresses in a network range.
   - MAC addresses are visible only within your network.

2. **TCP Connect Scan** (`-sT`):
   - Performs a full TCP 3-way handshake.
   - **Handshake Process**:
     - **SYN**: Initiate communication.
     - **SYN-ACK**: Acknowledge the initiation.
     - **ACK**: Confirm agreement on communication.

3. **TCP SYN Scan** (`-sS`):
   - A half-open scan that does not complete the handshake.
   - Considered stealthy but still detectable.

### Controlling Scan Speed

- **Timing Template** (`-T`): Adjusts the speed of the scan (0-5).
  - **0**: Low and slow.
  - **5**: Aggressive and noisy, faster results (default is 2-3).

### TCP Connection Flags

- **Flags for Various Scans**:
  - `-sN`: Null scan (no flags).
  - `-sF`: FIN scan (closes TCP session).
  - `-sX`: Xmas scan (flags FIN, PUSH, URGENT).

### Additional Options

- **Fast Mode** (`-F`): Scans fewer ports than default.
- **Port Ranges** (`-p`): Specify which ports to scan (e.g., `-p22; -p1-63535`).
- **Traceroute**: Can be added to display hops between you and the target.

### UDP Scanning

- **UDP Scan** (`-sU`): Does not establish connections but sends packets.

### Decoy and Spoofing Options

- **Decoy Scan** (`-D`): Utilizes a decoy host.
- **Zombie Host Scan** (`-sI`): Uses an idle scan technique to hide true IP.
- **Spoofed Source IP** (`-S`): Sends packets with a changed source IP.
- **Fragmented Packets** (`-f` or `--mtu`): Scans using fragmented packets, which can lead to issues if misused.

---

### Results Interpretation

- **Open Port**: Reliable, open, and reachable, awaiting connections.
- **Closed Port**: Responds with reset packets; no application accepting connections.
- **Filtered Port**: Cannot be probed, usually due to a firewall.
- **Unfiltered Port**: Reachable, but status (open/closed) cannot be determined.
- **Open/Filtered Port**: Limited scan (e.g., UDP) prevents determination.
- **Closed/Filtered Port**: Status undetermined due to idle scans or decoy scans.

---

## Alternative Tools

### Hping

- **Description**: A powerful packet spoofing utility (hping3 in command line).
- **Ack Scan**: Sends packets without the SYN flag; can indicate open ports by receiving reset responses.

### Responder

- **Function**: A Man-in-the-Middle (MiTM) tool for detecting vulnerabilities to LLMNR attacks.
- **Overview**: Intercepts requests and injects spoofed responses if Windows falls back to other name resolution methods when DNS fails.

---

This organized structure provides clarity on vulnerability identification methods and tools, making it easier to reference and understand these concepts. Let me know if you need further adjustments or specific details!