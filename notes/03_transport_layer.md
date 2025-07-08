# Transport Layer in Computer Networks (Expanded)

---

## Purpose of the Transport Layer
The transport layer ensures that data is delivered from one application to another reliably, in order, and without errors (if needed). It acts as a delivery service between programs running on different computers.

**Analogy:** Like a courier company that guarantees your package arrives safely and in the right order.

---

## TCP (Transmission Control Protocol)
- **Connection-oriented:** Establishes a connection before sending data (3-way handshake: SYN, SYN-ACK, ACK)
- **Reliable:** Guarantees delivery, correct order, and no duplicates
- **Flow Control:** Prevents sender from overwhelming receiver (window size)
- **Congestion Control:** Adjusts sending rate to avoid network overload
- **Use Cases:** Web browsing, email, file transfer
- **Analogy:** Like sending registered mail with tracking and delivery confirmation

### How TCP Works (Step-by-Step)
1. **Connection Setup:** 3-way handshake
2. **Data Transfer:** Data is broken into segments, sent, acknowledged
3. **Flow & Congestion Control:** Sender adjusts speed based on feedback
4. **Connection Teardown:** Graceful close (FIN, ACK)

---

## UDP (User Datagram Protocol)
- **Connectionless:** No setup, just send data
- **Unreliable:** No guarantee of delivery, order, or error checking
- **Fast and lightweight:** Less overhead
- **Use Cases:** Streaming, gaming, VoIP
- **Analogy:** Like sending postcards—fast, but no delivery confirmation

---

## Reliable Data Transfer Algorithms

### Stop-and-Wait ARQ
- Sender sends one packet, waits for ACK before sending next
- **Example:** Mailing a letter and waiting for a reply before sending another

### Go-Back-N ARQ
- Sender can send several packets before needing an ACK, but must resend all packets after a lost one
- **Example:** Sending a series of letters, but if one is lost, you resend that one and all after it

### Selective Repeat ARQ
- Only the lost or corrupted packets are resent
- **Example:** Resending only the missing pages of a book, not the whole book

---

## Flow Control
- Prevents sender from sending too much data too quickly
- **TCP Window Size:** Receiver tells sender how much data it can handle
- **Analogy:** Pouring water slowly so the glass doesn’t overflow

---

## Congestion Control
- Prevents network overload by adjusting sending rate
- **Algorithms:**
  - **TCP Tahoe:** Slow start, congestion avoidance, fast retransmit
  - **TCP Reno:** Adds fast recovery
  - **TCP NewReno:** Improves fast recovery
  - **TCP Selective ACK (SACK):** Only resend missing segments
  - **TCP CUBIC:** Used in modern systems, better for high-speed networks
  - **ECN (Explicit Congestion Notification):** Routers mark packets instead of dropping
  - **QUIC:** Modern protocol by Google, combines reliability and speed
- **Analogy:** Like adjusting traffic lights to prevent traffic jams

---

## Timers and Retransmission
- **RTO (Retransmission Time-out):** Timer for waiting on ACKs
- **ACK Ambiguity:** Hard to tell which packet an ACK is for
- **RTT Spread:** Variation in round-trip times
- **Nagle’s Algorithm:** Combines small packets to avoid Silly Window Syndrome
- **Silly Window Syndrome:** Sending tiny packets wastes bandwidth

---

## Step-by-Step: TCP 3-Way Handshake
1. **SYN:** Client sends SYN to server to request connection.
2. **SYN-ACK:** Server replies with SYN-ACK to acknowledge and agree.
3. **ACK:** Client sends ACK to confirm connection is established.

**Diagram:** [Client] --SYN--> [Server] --SYN-ACK--> [Client] --ACK--> [Server]

---

## Step-by-Step: TCP Flow Control
1. Sender checks receiver’s advertised window size.
2. Sender sends only as much data as fits in the window.
3. Receiver sends ACKs and updates window size as it processes data.
4. Sender adjusts sending rate based on window size.

**Diagram:** [Sender] --(data, window size)--> [Receiver]

---

## Step-by-Step: TCP Congestion Control (Tahoe Example)
1. Start with small congestion window (cwnd).
2. Increase cwnd exponentially (slow start) until threshold.
3. Switch to linear increase (congestion avoidance).
4. On packet loss (timeout), reset cwnd to 1, halve threshold.
5. Repeat process.

**Diagram:** cwnd vs time graph (slow start, congestion avoidance, loss)

---

## Step-by-Step: Stop-and-Wait ARQ
1. Sender sends one packet, starts timer.
2. Waits for ACK from receiver.
3. If ACK received, send next packet.
4. If timer expires, resend packet.

---

## Step-by-Step: Go-Back-N ARQ
1. Sender can send multiple packets (window size N) before needing ACK.
2. If a packet is lost, all subsequent packets are resent.
3. Receiver only accepts packets in order.

---

## Step-by-Step: Selective Repeat ARQ
1. Sender can send multiple packets (window size N).
2. Receiver accepts out-of-order packets, buffers them.
3. Only lost/corrupted packets are resent.

---

## Step-by-Step: TCP Timers and Retransmissions
1. Sender starts timer for each unacknowledged segment.
2. If ACK received before timer expires, stop timer.
3. If timer expires, retransmit segment.
4. Adjust timer based on measured RTT.

---

## Summary Table: Transport Layer Protocols & Features
| Protocol/Algorithm | Reliable? | Connection? | Use Case                |
|--------------------|-----------|-------------|-------------------------|
| TCP                | Yes       | Yes         | Web, email, file xfer   |
| UDP                | No        | No          | Streaming, games, VoIP  |
| Stop-and-Wait ARQ  | Yes       | Yes         | Simple links            |
| Go-Back-N ARQ      | Yes       | Yes         | Moderate links          |
| Selective Repeat   | Yes       | Yes         | High-speed links        |
| SACK               | Yes       | Yes         | Efficient TCP recovery  |
| Nagle's Algorithm  | Yes       | Yes         | Avoids tiny packets     |
| CUBIC, Reno, etc.  | Yes       | Yes         | Congestion control      |

---

## Troubleshooting Transport Layer Issues
- **Connection Drops:** Check for firewall, NAT, or port issues
- **Slow Transfer:** Check for congestion, window size, retransmissions
- **Packet Loss:** Check for network errors, congestion, ARQ settings
- **Out-of-Order Delivery:** May be normal for UDP, check for reordering in TCP

---

## More Real-World Scenarios
- **File Download:** Uses TCP for reliability, ARQ for retransmission
- **Live Stream:** Uses UDP for speed, may tolerate some loss
- **Online Game:** Uses UDP for low latency, app handles errors

---

## Top 10 Exam Mistakes (Transport Layer)
1. Mixing up TCP and UDP
2. Forgetting ARQ types and how they work
3. Not knowing what SACK or Nagle's Algorithm do
4. Confusing flow control and congestion control
5. Ignoring the 3-way handshake steps
6. Overlooking timer and retransmission logic
7. Not understanding window size effects
8. Forgetting what causes Silly Window Syndrome
9. Not knowing how congestion control algorithms differ
10. Skipping Q&A practice

---

# (All key processes are now explained step-by-step. All concepts are clarified.) 