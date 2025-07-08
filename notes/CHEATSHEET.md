# Computer Networks Cheat Sheet (Ultimate Exam Edition)

---

## Network Types
- **LAN:** Local, small area (home, office)
- **WAN:** Wide, large area (internet)
- **PAN:** Personal, very short range (Bluetooth)
- **MAN:** Metropolitan, city-wide

---

## OSI & Internet Model Layers
| OSI Layer         | Internet Model | Key Function                |
|-------------------|---------------|-----------------------------|
| Application (7)   | Application   | User apps (web, email)      |
| Presentation (6)  | Application   | Formatting, encryption      |
| Session (5)       | Application   | Sessions, connections       |
| Transport (4)     | Transport     | TCP/UDP, reliability        |
| Network (3)       | Network       | IP, routing                 |
| Data Link (2)     | Link          | Frames, MAC, error detect   |
| Physical (1)      | Physical      | Cables, signals             |

---

## Key Protocols, Ports & Concepts
| Protocol | Port | Description                  |
|----------|------|------------------------------|
| HTTP     | 80   | Web browsing                 |
| HTTPS    | 443  | Secure web                   |
| FTP      | 21   | File transfer                |
| DNS      | 53   | Name resolution              |
| SMTP     | 25   | Email sending                |
| POP3     | 110  | Email receiving              |
| IMAP     | 143  | Email receiving (advanced)   |
| SSH      | 22   | Secure shell                 |
| Telnet   | 23   | Remote login (insecure)      |
| DHCP     | 67/68| Dynamic IP assignment        |
| SNMP     | 161  | Network management           |
| RIP      | 520  | Routing                      |
| OSPF     | -    | Routing (no fixed port)      |
| TCP      | -    | Reliable transport           |
| UDP      | -    | Fast, connectionless         |

---

## Addressing
- **MAC Address:** Hardware, local delivery (e.g., 00:1A:2B:3C:4D:5E)
- **IP Address:** Logical, global delivery (IPv4: 192.168.1.1, IPv6: 2001:...)
- **Subnet Mask:** Defines network/subnet (e.g., 255.255.255.0)

---

## Error Detection
- **Parity Bit:** Detects single-bit errors
- **Checksum:** Sums data, detects errors
- **CRC:** Powerful, used in Ethernet/WiFi

---

## Routing
- **Dijkstra:** Link-state, shortest path
- **Bellman-Ford:** Distance-vector
- **RIP:** Distance-vector, slow updates
- **OSPF:** Link-state, fast updates
- **NAT:** Shares one public IP among many
- **RPF:** Multicast, shortest path check

---

## Transport Layer
- **Stop-and-Wait:** One packet at a time
- **Go-Back-N:** Multiple, resend after loss
- **Selective Repeat:** Only resend lost
- **TCP Flow Control:** Window size
- **Congestion Control:** Tahoe, Reno, CUBIC, etc.
- **Nagle’s Algorithm:** Combines small packets
- **Silly Window Syndrome:** Wastes bandwidth

---

## Wireless & Multimedia
- **WiFi (802.11):** Wireless LAN, uses CSMA/CA
- **Cellular:** Mobile, uses handoff
- **CDN:** Distributes content for streaming
- **QoS:** Prioritizes multimedia traffic
- **RTP/RTCP/SIP:** Real-time audio/video

---

## Security
- **Encryption:** Scrambles data
- **Symmetric/Asymmetric:** One key vs. public/private
- **Firewall:** Blocks unwanted traffic
- **IDS:** Detects suspicious activity
- **SYN Flooding:** DoS attack on servers

---

## Must-Know Formulas
- **Subnetting:**
  - Number of hosts = 2^(32 - subnet bits) - 2
  - Subnet mask for n bits: 255.255.255.0 (for /24)
- **Throughput:**
  - Throughput = File size / Transfer time
- **Delay:**
  - Total delay = Transmission + Propagation + Queuing + Processing
  - Transmission delay = Packet size / Link bandwidth
  - Propagation delay = Distance / Propagation speed
- **Utilization (Stop-and-Wait):**
  - U = (Transmission time) / (Transmission time + 2 * Propagation time)

---

## Key Differences (Exam Table)
| Topic         | Option 1 | Option 2 | Key Difference                |
|---------------|----------|----------|-------------------------------|
| TCP vs UDP    | TCP      | UDP      | Reliable, ordered vs fast     |
| LAN vs WAN    | LAN      | WAN      | Local vs wide area            |
| RIP vs OSPF   | RIP      | OSPF     | Distance-vector vs link-state |
| IPv4 vs IPv6  | IPv4     | IPv6     | 32-bit vs 128-bit addresses   |
| Switch vs Hub | Switch   | Hub      | Smart forwarding vs broadcast |

---

## Glossary: Must-Know Terms
- **Host:** Any device on a network
- **Router:** Directs data between networks
- **Switch:** Connects devices in a LAN
- **Protocol:** Rules for communication
- **Packet:** Data unit at network layer
- **Frame:** Data unit at link layer
- **MAC Address:** Hardware address
- **IP Address:** Logical address
- **Port:** Identifies app/service
- **Bandwidth:** Max data rate
- **Latency:** Delay in transfer
- **Throughput:** Actual data rate
- **Topology:** Network layout

---

## Exam Tips
- Draw diagrams for protocols and flows
- Know differences: TCP vs UDP, LAN vs WAN, RIP vs OSPF, IPv4 vs IPv6
- Practice subnetting and addressing
- Review error detection and congestion control
- Understand real-world examples (YouTube, BitTorrent, WiFi)
- Memorize key port numbers and protocol functions
- Use the OSI model to troubleshoot network issues 