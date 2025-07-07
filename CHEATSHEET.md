# Computer Networking Final Exam Cheatsheet

---

## Chapter 1: Introduction & Foundations
- **Internet:** Global network, connects billions of devices
- **Key Concepts:** Network edge/core, protocols, delay, loss, throughput, security, history
- **Network Types:** LAN, MAN, WAN (distance, speed, ownership)
- **Physical Media:** Twisted pair, coaxial, fiber, wireless
- **WAN Technologies:** Circuit-switched, packet-switched, broadband
- **Data Transmission:** Bits, bytes, ASCII, signals (electrical, optical, wireless)
- **Bandwidth/Throughput:** Units (bps, kbps, Mbps, Gbps), actual vs theoretical
- **Protocols:** OSI vs TCP/IP, encapsulation, layering benefits
- **Security:** Attacks (DoS, malware, phishing), defense mechanisms
- **History:** ARPANET, TCP/IP, WWW, five development periods

**Tables:**
| Concept      | Key Point / Example         |
|--------------|----------------------------|
| Internet     | Global network             |
| Edge         | User devices, access       |
| Core         | Routers, backbone          |
| Delay        | Types, formulas            |
| Protocols    | OSI, TCP/IP, encapsulation |
| Attacks      | DoS, malware, phishing     |
| History      | ARPANET, TCP/IP, WWW       |

---

## Chapter 2: Application Layer
- **Architectures:** Client-server, P2P
- **Key Protocols:** HTTP, SMTP, POP3, IMAP, DNS, FTP
- **Concepts:** Sockets, streaming, CDN, email, P2P
- **Web/HTTP:** Stateless, persistent/non-persistent, cookies, caching
- **Email:** SMTP, POP3, IMAP, phases, features
- **DNS:** Hierarchy, root/TLD/authoritative/local servers, iterative queries
- **P2P:** BitTorrent, DHT, swarm, tracker, tit-for-tat
- **Video Streaming/CDN:** DASH, client intelligence, CDN strategies
- **Socket Programming:** TCP/UDP sockets, API, handshake

**Tables:**
| Concept      | Key Point / Example         |
|--------------|----------------------------|
| HTTP         | Web, stateless, TCP        |
| SMTP/POP3    | Email send/receive         |
| DNS          | Name to IP mapping         |
| P2P          | BitTorrent, scalable       |
| CDN          | Video streaming, edge      |

---

## Chapter 3: Transport Layer
- **Protocols:** TCP (reliable), UDP (unreliable)
- **Concepts:** Multiplexing, demultiplexing, reliable data transfer (RDT), flow/congestion control
- **TCP:** Connection establishment, flow control, congestion control (AIMD, slow start, Tahoe, Reno, New Reno, CUBIC, ECN, QUIC)
- **UDP:** Fast, connectionless, no guarantees
- **Timers:** RTO, ACK ambiguity, RTT spread
- **RDT:** Stop-and-wait, Go-Back-N, Selective Repeat
- **QUIC:** HTTP/3, streams, no HOL blocking

**Tables:**
| Concept      | Key Point / Example         |
|--------------|----------------------------|
| TCP          | Reliable, ordered, flow ctrl|
| UDP          | Unreliable, fast           |
| RDT          | ACK, NAK, timeouts         |
| Congestion   | TCP slow start, AIMD       |
| Multiplexing | Ports, sockets             |

---

## Chapter 4: Network Layer I (Data Plane)
- **Functions:** Routing, forwarding, addressing
- **Protocols:** IP (IPv4/IPv6), ICMP, NAT, SDN/OpenFlow
- **Router Architecture:** Input/output ports, switching fabric, buffer management (tail drop, RED, bufferbloat)
- **IP:** Datagram format, addressing, subnetting, VLSM, FLSM, fragmentation, reassembly
- **NAT:** Address sharing, operation, pros/cons
- **ICMP:** Echo, unreachable, time exceeded, redirect
- **IPv6:** Header, addressing, transition (dual stack, tunneling, NAT64)
- **SDN:** Control/data plane split, OpenFlow, use cases

**Tables:**
| Concept      | Key Point / Example         |
|--------------|----------------------------|
| Routing      | Path selection, routers    |
| Forwarding   | Next-hop, switching fabric |
| IP           | Addressing, datagram       |
| IPv6         | 128-bit, improved features |
| SDN          | Control/data plane split   |

---

## Chapter 5: Network Layer II (Control Plane)
- **Routing Algorithms:** Dijkstra (link-state), Bellman-Ford (distance-vector), count-to-infinity
- **Protocols:** OSPF (intra-AS), BGP (inter-AS), RIP
- **SDN Controllers:** ODL, ONOS, OpenFlow
- **ICMP:** Error reporting, diagnostics, traceroute
- **Network Management:** SNMP, NETCONF/YANG
- **Hierarchical Routing:** AS, area border routers
- **BGP Path Attributes:** AS-PATH, NEXT-HOP, LOCAL_PREF, MED

**Tables:**
| Concept      | Key Point / Example         |
|--------------|----------------------------|
| Routing      | Path selection, OSPF, BGP  |
| OSPF         | Link-state, intra-AS       |
| BGP          | Path vector, inter-AS      |
| SDN          | Control/data plane split   |
| ICMP         | Error reporting, ping      |
| SNMP         | Network management         |

---

## Chapter 6: Link Layer & Local Area Networks
- **Functions:** Framing, error detection/correction, medium access
- **Protocols:** Ethernet, WiFi, PPP, ARP, VLAN, MPLS
- **Error Detection:** Parity, checksum, CRC, Hamming
- **Multiple Access:** TDMA, FDMA, ALOHA, CSMA/CD, Token Ring
- **Switching:** Layer 2/3/multilayer, VLANs, port security
- **Hierarchical Design:** Access, distribution, core layers
- **Broadcast Containment:** VLANs, subnetting, storm control, ACLs
- **Data Center Topologies:** Fat-tree, spine-leaf, multi-rooted
- **Web Request Journey:** DHCP, ARP, DNS, TCP, HTTP, IP/Ethernet

**Tables:**
| Concept      | Key Point / Example         |
|--------------|----------------------------|
| Framing      | Encapsulate data in frames |
| CRC          | Error detection, Ethernet  |
| CSMA/CD      | Ethernet, collision detect |
| VLAN         | Logical segmentation       |
| MPLS         | Label switching, WANs      |
| Fat-tree     | Data center topology       |

---

## Chapter 7: Wireless & Mobile Networks
- **Wireless Impairments:** Fading, multipath, noise, hidden terminal
- **WiFi (802.11):** Standards, BSS, CSMA/CA, RTS/CTS, frame structure, rate adaptation
- **Cellular Networks:** 4G LTE architecture (UE, eNode-B, HSS, S-GW, P-GW, MME), 5G evolution (mmWave, MIMO, SDN)
- **Mobility Management:** Home/visited network, registration, handoff, GTP tunneling
- **Mobile IP:** Home/foreign agent, tunneling, registration
- **TCP Impact:** Loss, delay, split connections
- **Solutions:** Link-layer retransmissions, adaptive streaming

**Tables:**
| Concept      | Key Point / Example         | Details                    |
|--------------|----------------------------|----------------------------|
| WiFi         | 802.11, CSMA/CA, WPA2      | 802.11ax: 14 Gbps, 2.4/5 GHz|
| Cellular     | Cells, handoff, MSC        | 4G LTE: MME, HSS, P-GW, S-GW|
| Mobility     | Home/care-of address, reg. | Indirect vs direct routing |
| Mobile IP    | Tunneling, home/foreign ag.| Historical, limited adoption|
| Handoff      | Hard/soft, location mgmt   | GTP tunneling, 4G handover |
| TCP Impact   | Loss, delay, split conn.   | Congestion control issues  |
| 5G           | 10x speed, 10x latency     | mmWave, MIMO, pico-cells  |

---

## Chapter 8: Network Security
- **Goals:** Confidentiality, authentication, integrity, availability
- **Cryptography:** Symmetric (AES, DES), asymmetric (RSA, ECC), hash (SHA, MD5)
- **Authentication:** Passwords, tokens, biometrics, certificates
- **Digital Signatures:** Non-repudiation, integrity
- **PKI:** Certificate authorities, key management
- **Protocols:** SSL/TLS, IPsec, WPA2/WPA3, PGP, S/MIME
- **Security Devices:** Firewalls, IDS/IPS, gateways
- **Operational Security:** ACLs, DMZ, VPNs, security zones
- **Incident Response:** Detection, analysis, containment, recovery

**Tables:**
| Concept      | Key Point / Example         | Security Property    |
|--------------|----------------------------|---------------------|
| Cryptography | Encryption, decryption     | Confidentiality     |
| Authentication| Verify identity           | Identity verification|
| Integrity    | Data hasn't changed        | Tamper detection    |
| Firewalls    | Traffic filtering          | Access control      |
| IDS/IPS      | Intrusion detection        | Threat monitoring   |
| SSL/TLS      | Secure web communication   | End-to-end security |
| VPNs         | Secure remote access       | Tunnel security     |
| IPsec        | Network layer security     | Packet-level security|
| WPA3         | Wireless security          | Link-level security |

---

## Chapter 9: Multimedia Networking
- **Applications:** Streaming (YouTube, Netflix), VoIP (Skype, WhatsApp)
- **Protocols:** RTP, RTCP, SIP, H.323, HTTP streaming
- **Network Support:** Scheduling, policing, QoS (IntServ, DiffServ, RSVP), resource reservation
- **Buffering:** Handles jitter/delay
- **CDN:** Scalable video delivery
- **Adaptive Streaming:** DASH, HLS
- **Codecs:** G.711, G.729, Opus, H.264, H.265
- **Traffic Shaping/Policing:** Leaky bucket, token bucket
- **Multicast Routing:** IGMP, PIM
- **Error Recovery:** FEC, interleaving, retransmission

**Tables:**
| Concept      | Key Point / Example         |
|--------------|----------------------------|
| Streaming    | YouTube, Netflix           |
| VoIP         | Skype, WhatsApp            |
| RTP/RTCP     | Media transport/feedback   |
| SIP/H.323    | Session management         |
| Buffering    | Handles jitter/delay       |
| CDN          | Scalable video delivery    |
| QoS          | Scheduling, policing       |

---

## High-Weightage & Missing Topics (from Syllabus & missing_topics.md)
- **WiFi, Ethernet, CSMA/CD, CSMA/CA:** Ch6, Ch7
- **Checksum, CRC, Parity Checking:** Ch6
- **RPF, DVMRP, PIM:** See missing_topics.md & Ch9
- **Count-to-infinity, Bellman-Ford, Dijkstra:** Ch5
- **RIP, OSPF:** Ch5
- **IPv6, ICMPv6, IPv4 Subnetting, NAT:** Ch4, Ch5
- **IP Fragmentation, Datagram Segmentation:** Ch4
- **IPv4/IPv6 Transition:** Ch4
- **Queuing, FIFO, Fair Queuing, RED:** Ch4, Ch9
- **TCP Congestion Control, Tahoe, Reno, New Reno, CUBIC, ECN, QUIC:** Ch3
- **TCP Timers, RTO, ACK ambiguity, RTT:** Ch3
- **TCP Flow Control, Silly-window Syndrome, Nagle's Algorithm:** Ch3, missing_topics.md
- **Reliable Data Transfer, Stop-and-wait, Go-Back-N, Selective Repeat:** Ch3
- **TCP Connection Establishment, SYN Flooding Attack:** Ch3, missing_topics.md
- **P2P, BitTorrent:** Ch2, missing_topics.md
- **Client-Server, DNS, FTP, Email, HTTP, Proxy:** Ch2, Ch7

---

## Diagrams & Mind Maps
- Use the mind maps and diagrams from each chapter summary for visual revision (see chapter summaries for mermaid diagrams).
- Practice drawing protocol stacks, encapsulation, routing, switching, and security diagrams.

---

## Exam Tips
- Focus on definitions, diagrams, and formulas.
- Practice explaining concepts with analogies.
- Avoid common mistakes listed in each chapter summary.
- Memorize protocol features, network types, and key algorithms.
- Be able to compare/contrast protocols, technologies, and architectures.
- Use tables and mind maps for last-minute revision.

---

## Abbreviations & Full Forms Reference

| Abbreviation | Full Form |
|--------------|-----------|
| 4G | Fourth Generation (Mobile Network) |
| 5G | Fifth Generation (Mobile Network) |
| ACK | Acknowledgment |
| AIMD | Additive Increase Multiplicative Decrease |
| API | Application Programming Interface |
| ARP | Address Resolution Protocol |
| AS | Autonomous System |
| AS-PATH | Autonomous System Path |
| ASCII | American Standard Code for Information Interchange |
| BGP | Border Gateway Protocol |
| BSS | Basic Service Set |
| CDN | Content Delivery Network |
| CIDR | Classless Inter-Domain Routing |
| CRC | Cyclic Redundancy Check |
| CSMA/CD | Carrier Sense Multiple Access with Collision Detection |
| CSMA/CA | Carrier Sense Multiple Access with Collision Avoidance |
| DHT | Distributed Hash Table |
| DHCP | Dynamic Host Configuration Protocol |
| DMZ | Demilitarized Zone |
| DNS | Domain Name System |
| DoS | Denial of Service |
| DVMRP | Distance Vector Multicast Routing Protocol |
| ECN | Explicit Congestion Notification |
| FEC | Forward Error Correction |
| FLSM | Fixed Length Subnet Masking |
| FTP | File Transfer Protocol |
| Gbps | Gigabits per second |
| GTP | GPRS Tunneling Protocol |
| H.323 | ITU-T Recommendation H.323 (VoIP standard) |
| HSS | Home Subscriber Service |
| HOL | Head of Line |
| HTTP | HyperText Transfer Protocol |
| HTTPS | HyperText Transfer Protocol Secure |
| ICMP | Internet Control Message Protocol |
| ICMPv6 | Internet Control Message Protocol version 6 |
| IDS | Intrusion Detection System |
| IMAP | Internet Message Access Protocol |
| IGMP | Internet Group Management Protocol |
| IP | Internet Protocol |
| IPsec | Internet Protocol Security |
| IPv4 | Internet Protocol version 4 |
| IPv6 | Internet Protocol version 6 |
| ISP | Internet Service Provider |
| LAN | Local Area Network |
| MAC | Media Access Control |
| MAN | Metropolitan Area Network |
| Mbps | Megabits per second |
| MED | Multi-Exit Discriminator |
| MIMO | Multiple Input Multiple Output |
| MPLS | Multi-Protocol Label Switching |
| MSC | Mobile Switching Center |
| NAT | Network Address Translation |
| NETCONF | Network Configuration Protocol |
| NAK | Negative Acknowledgment |
| ODL | OpenDaylight (SDN Controller) |
| OFDM | Orthogonal Frequency Division Multiplexing |
| OSPF | Open Shortest Path First |
| P2P | Peer-to-Peer |
| P-GW | Packet Data Network Gateway |
| PGP | Pretty Good Privacy |
| PIM | Protocol Independent Multicast |
| PKI | Public Key Infrastructure |
| POP3 | Post Office Protocol 3 |
| PPP | Point-to-Point Protocol |
| QoS | Quality of Service |
| QUIC | Quick UDP Internet Connections |
| RDT | Reliable Data Transfer |
| RED | Random Early Detection |
| RFC | Request for Comments |
| RIP | Routing Information Protocol |
| RPF | Reverse Path Forwarding |
| RTO | Retransmission Timeout |
| RTS/CTS | Request to Send / Clear to Send |
| RTP | Real-time Transport Protocol |
| RTCP | Real-time Transport Control Protocol |
| RSVP | Resource Reservation Protocol |
| SDN | Software Defined Networking |
| S-GW | Serving Gateway |
| SHA | Secure Hash Algorithm |
| SIFS/DIFS | Short/Distributed Interframe Space |
| SMTP | Simple Mail Transfer Protocol |
| SNMP | Simple Network Management Protocol |
| SSL | Secure Sockets Layer |
| SYN | Synchronize (TCP flag) |
| TCP | Transmission Control Protocol |
| TLD | Top Level Domain |
| TLS | Transport Layer Security |
| TDMA | Time Division Multiple Access |
| UDP | User Datagram Protocol |
| UE | User Equipment |
| VLAN | Virtual Local Area Network |
| VLSM | Variable Length Subnet Masking |
| VoIP | Voice over Internet Protocol |
| VPN | Virtual Private Network |
| WAN | Wide Area Network |
| WPA2/WPA3 | Wi-Fi Protected Access 2/3 |
| WWW | World Wide Web | 