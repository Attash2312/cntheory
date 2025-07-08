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

---

# Abbreviations & Full Forms
| Abbreviation | Full Form                        | Description/Use                        |
|--------------|----------------------------------|----------------------------------------|
| TCP          | Transmission Control Protocol    | Reliable, connection-oriented transport|
| UDP          | User Datagram Protocol           | Fast, connectionless transport         |
| ARP          | Address Resolution Protocol      | Maps IP to MAC in LAN                  |
| NAT          | Network Address Translation      | Shares one public IP among many        |
| VLAN         | Virtual Local Area Network       | Logical segmentation of LAN            |
| OSPF         | Open Shortest Path First         | Link-state routing protocol            |
| RIP          | Routing Information Protocol     | Distance-vector routing protocol       |
| BGP          | Border Gateway Protocol          | Inter-domain routing (Internet)        |
| ICMP         | Internet Control Message Protocol| Error messages, diagnostics (ping)     |
| DNS          | Domain Name System               | Name to IP translation                 |
| FTP          | File Transfer Protocol           | Transfers files between computers      |
| SMTP         | Simple Mail Transfer Protocol    | Email sending                          |
| POP3         | Post Office Protocol v3          | Email receiving (download & delete)    |
| IMAP         | Internet Message Access Protocol | Email receiving (sync, keep on server) |
| SSL/TLS      | Secure Sockets Layer/Transport Layer Security | Secure web, encryption      |
| VPN          | Virtual Private Network          | Secure, private connection over public |
| IDS/IPS      | Intrusion Detection/Prevention System | Detects/prevents attacks         |
| SACK         | Selective Acknowledgment         | Efficient TCP retransmission           |
| CDN          | Content Delivery Network         | Distributes content for fast delivery  |
| QoS          | Quality of Service               | Prioritizes network traffic            |
| CSMA/CD      | Carrier Sense Multiple Access/Collision Detection | Ethernet collision mgmt   |
| CSMA/CA      | Carrier Sense Multiple Access/Collision Avoidance | WiFi collision avoidance |
| DHCP         | Dynamic Host Configuration Protocol | Assigns IP addresses automatically |
| PKI          | Public Key Infrastructure        | Manages public keys/certificates       |
| RTP/RTCP     | Real-Time Protocol/Control       | Real-time audio/video, feedback        |
| SIP          | Session Initiation Protocol      | Sets up/tears down calls               |
| RED          | Random Early Detection           | Congestion avoidance in routers        |
| ECN          | Explicit Congestion Notification | Congestion signal without dropping     |
| QUIC         | Quick UDP Internet Connections   | Fast, secure transport (HTTP/3)        |
| DVMRP        | Distance Vector Multicast Routing Protocol | Multicast routing              |
| PIM          | Protocol Independent Multicast   | Multicast tree building                |
| RPF          | Reverse Path Forwarding          | Multicast path check                   |
| AP           | Access Point                     | WiFi base station                      |
| MTU          | Maximum Transmission Unit        | Largest frame/packet size allowed      |
| RTT          | Round-Trip Time                  | Time for packet to go and return       |
| FLSM/VLSM    | Fixed/Variable Length Subnet Mask| Subnetting methods                     |
| ...          | ...                              | ...                                    |

---

# Comparison Tables & Pros/Cons

## TCP vs UDP
| Feature         | TCP                          | UDP                        |
|-----------------|-----------------------------|----------------------------|
| Reliability     | Yes (guaranteed delivery)    | No (best effort)           |
| Connection      | Connection-oriented          | Connectionless             |
| Speed           | Slower (more overhead)       | Faster (less overhead)     |
| Use Cases       | Web, email, file transfer    | Streaming, games, VoIP     |
| Flow Control    | Yes                          | No                         |
| Congestion Ctrl | Yes                          | No                         |
| Pros            | Reliable, ordered, error-checked | Fast, simple, low latency |
| Cons            | Slower, more complex         | Unreliable, unordered      |
| When to Use     | When reliability/order matter| When speed/latency matter  |
| Flaws           | Overhead, slower             | No guarantee of delivery   |

---

## OSPF vs RIP
| Feature         | OSPF                         | RIP                        |
|-----------------|-----------------------------|----------------------------|
| Algorithm       | Link-state (Dijkstra)        | Distance-vector (Bellman)  |
| Convergence     | Fast                         | Slow                       |
| Scalability     | High                         | Low                        |
| Metric          | Cost (bandwidth)             | Hop count                  |
| Updates         | On change                    | Every 30 seconds           |
| Pros            | Efficient, scalable, fast    | Simple, easy to configure  |
| Cons            | More complex, uses more CPU  | Slow, not scalable         |
| When to Use     | Large/complex networks       | Small/simple networks       |
| Flaws           | Complexity                   | Slow convergence, loops    |

---

## IPv4 vs IPv6
| Feature         | IPv4                         | IPv6                       |
|-----------------|-----------------------------|----------------------------|
| Address Size    | 32 bits                      | 128 bits                   |
| Address Space   | ~4 billion                   | Virtually unlimited        |
| Notation        | Dotted decimal               | Hexadecimal                |
| NAT Needed      | Yes                          | No                         |
| Security        | Optional (IPsec)             | Built-in (IPsec)           |
| Pros            | Simple, widely used          | More addresses, security   |
| Cons            | Address exhaustion           | Not backward compatible    |
| When to Use     | Legacy, current internet     | Future, new deployments    |
| Flaws           | Limited addresses            | Transition complexity      |

---

## Switch vs Hub
| Feature         | Switch                       | Hub                        |
|-----------------|-----------------------------|----------------------------|
| Forwarding      | To specific device (MAC)     | Broadcast to all           |
| Collision Domain| Per port                     | One big domain             |
| Speed           | Faster, full duplex          | Slower, half duplex        |
| Security        | More secure                  | Less secure                |
| Pros            | Efficient, secure, scalable  | Cheap, simple              |
| Cons            | More expensive               | Not used in modern nets    |
| When to Use     | Modern LANs                  | Legacy only                |
| Flaws           | Cost                         | Collisions, inefficiency   |

---

## CSMA/CD vs CSMA/CA
| Feature         | CSMA/CD (Ethernet)           | CSMA/CA (WiFi)             |
|-----------------|-----------------------------|----------------------------|
| Collision Mgmt  | Detects, then retransmits    | Avoids, then transmits     |
| Medium          | Wired                        | Wireless                   |
| Use             | Ethernet LAN                 | WiFi LAN                   |
| Pros            | Simple, effective for wires  | Works for wireless         |
| Cons            | Not for wireless             | More overhead, less efficient |
| When to Use     | Wired LANs                   | Wireless LANs              |
| Flaws           | Can't avoid all collisions   | Overhead, hidden node      |

---

## More Comparisons (Quick Reference)
- **SMTP vs POP3 vs IMAP:** SMTP sends email; POP3 downloads and deletes; IMAP syncs and keeps on server.
- **RIP vs OSPF vs BGP:** RIP is simple, OSPF is scalable, BGP is for the internet.
- **Symmetric vs Asymmetric Encryption:** Symmetric is fast, one key; asymmetric is secure, two keys.
- **Firewall vs IDS/IPS:** Firewall blocks traffic; IDS/IPS detects/prevents attacks.
- **CDN vs Proxy:** CDN distributes content; proxy caches/filters content.

---

# Mnemonics & Memory Aids

- **OSI Layers:**
  - "Please Do Not Throw Sausage Pizza Away" (Physical, Data Link, Network, Transport, Session, Presentation, Application)
- **TCP/UDP Port Numbers:**
  - 80 = HTTP, 443 = HTTPS, 21 = FTP, 53 = DNS, 25 = SMTP, 110 = POP3, 143 = IMAP, 22 = SSH
- **Routing Protocols:**
  - "RIP is simple, OSPF is scalable, BGP is for the Internet"
- **Subnetting:**
  - "Slash = Subtract = Hosts" (e.g., /26 → 32-26=6, 2^6=64 addresses)

---

# Mind Maps & Flowcharts (Text-Based)

## OSI Model Mind Map
- Application
  - Presentation
    - Session
      - Transport
        - Network
          - Data Link
            - Physical

## Routing Decision Flow
- Packet arrives → Check destination IP → Routing table lookup → Best match? → Forward to next hop → Repeat until destination

## TCP/UDP Workflow
- TCP: Connection setup (3-way handshake) → Data transfer (ACKs, flow/congestion control) → Connection close
- UDP: No setup → Send data → No ACKs, no guarantee

## Troubleshooting Flow
- Start at Physical (cables, signal) → Data Link (MAC, switch) → Network (IP, routing) → Transport (TCP/UDP, ports) → Application (settings, credentials)

---

# Exam Traps & Quick Wins

## OSI Layers
- 🚩 **Trap:** Mixing up order (Physical is bottom, Application is top)
- ✅ **Quick Win:** Memorize mnemonic!

## TCP vs UDP
- 🚩 **Trap:** Saying UDP is always better for speed—sometimes reliability is more important!
- ✅ **Quick Win:** TCP = Reliable, UDP = Fast

## Subnetting
- 🚩 **Trap:** Forgetting to subtract 2 for network/broadcast addresses
- ✅ **Quick Win:** Hosts = 2^(32 - subnet bits) - 2

## VLAN vs Subnet
- 🚩 **Trap:** VLAN is at Data Link, Subnet is at Network layer
- ✅ **Quick Win:** VLAN = Switch, Subnet = Router

## NAT
- 🚩 **Trap:** Thinking NAT provides security—it mainly provides address sharing
- ✅ **Quick Win:** NAT = Many private IPs, one public IP

---

# Practice Problems & Answers

## Subnetting
- **Q:** How many usable hosts in a /27 subnet?
- **A:** 2^(32-27) - 2 = 30

## Delay Calculation
- **Q:** What is the total delay for a 1MB file over a 10Mbps link with 50ms propagation?
- **A:** Transmission = 8Mb/10Mbps = 0.8s; Total = 0.8s + 0.05s = 0.85s

## Throughput
- **Q:** If a 10MB file takes 20s to transfer, what is the throughput?
- **A:** 10MB/20s = 0.5MBps = 4Mbps

## TCP Window
- **Q:** If bandwidth is 5Mbps and RTT is 100ms, what is the optimal window size?
- **A:** 5Mbps × 0.1s = 0.5Mb = 62.5KB

## Routing Table Lookup
- **Q:** If a router has entries for 192.168.1.0/24 and 192.168.1.0/25, which is used for 192.168.1.100?
- **A:** 192.168.1.0/25 (longest prefix match)

## Error Detection
- **Q:** What is the parity bit for 1010110 (even parity)?
- **A:** 1 (to make total number of 1s even)

---

# If You See This in the Exam...
- **"3-way handshake"** → Think TCP connection setup (SYN, SYN-ACK, ACK)
- **"Hidden node"** → Think WiFi, CSMA/CA
- **"Hop count"** → Think RIP, distance-vector
- **"Link-state"** → Think OSPF, Dijkstra
- **"Selective ACK"** → Think TCP SACK, efficient retransmission
- **"NAT"** → Think address sharing, not security
- **"Jitter"** → Think multimedia, real-time traffic
- **"TTL expired"** → Think ICMP, traceroute

---

# Emoji Highlights
- ✅ = Quick Win / Pro Tip
- 🚩 = Common Mistake / Exam Trap
- 💡 = Important Concept
- 🔥 = High-Yield for Exam

---

# (This CHEATSHEET now includes mnemonics, mind maps, exam traps, quick wins, practice problems, and more for the best possible revision!) 