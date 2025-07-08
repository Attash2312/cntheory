# Routing in Computer Networks

---

## Introduction to Routing
Routing is like planning a road trip: it’s the process of finding the best path for data to travel from one device to another across a network.

- **Routers** are devices that make these decisions, forwarding data from one network to another.
- **Analogy:** Like traffic cops at intersections, routers decide which road (network path) your data should take next.

---

## Routing Algorithms

### 1. Dijkstra’s Algorithm (Link-State)
- Finds the shortest path from a source to all other nodes.
- Each router knows the entire network map.
- **Analogy:** Like using Google Maps with real-time traffic info to find the fastest route.
- **Steps:**
  1. Start at the source node.
  2. Mark the distance to itself as 0, all others as infinity.
  3. Visit the nearest unvisited node, update distances to neighbors.
  4. Repeat until all nodes are visited.

### 2. Bellman-Ford Algorithm (Distance-Vector)
- Each router only knows the distance to its neighbors.
- Routers share their distance tables with neighbors.
- **Analogy:** Like asking your friends how far they are from a destination, and updating your own estimate.
- **Steps:**
  1. Each router starts with its own distance to neighbors.
  2. Routers exchange info and update their tables.
  3. Repeat until no more updates.

### 3. Count-to-Infinity Problem
- A problem in distance-vector routing where routers keep increasing the distance to a destination that’s become unreachable.
- **Analogy:** Like a rumor spreading in a circle, never reaching the truth.

---

## RIP and OSPF

### RIP (Routing Information Protocol)
- Uses distance-vector (Bellman-Ford) algorithm.
- Routers share their tables every 30 seconds.
- Simple, but slow to react to changes.

### OSPF (Open Shortest Path First)
- Uses link-state (Dijkstra) algorithm.
- Routers share only changes, not full tables.
- Faster and more scalable than RIP.

---

## Multicast Routing

### RPF (Reverse Path Forwarding)
- Ensures multicast packets follow the shortest path from the source.
- **Analogy:** Like only accepting a package if it arrives by the shortest route from the sender.

### DVMRP (Distance Vector Multicast Routing Protocol)
- Uses distance-vector info to build multicast trees.
- Prunes branches with no group members.

### PIM (Protocol Independent Multicast)
- Builds multicast trees using info from other routing protocols.
- Used for efficient group communication (e.g., live video streaming).

---

## Summary
- Routing finds the best path for data across networks.
- Dijkstra and Bellman-Ford are key algorithms.
- RIP and OSPF are common routing protocols.
- Multicast routing delivers data to multiple recipients efficiently.

---

## Exam-Style Q&A

**Q1:** What is the main difference between Dijkstra and Bellman-Ford algorithms?
**A1:** Dijkstra knows the whole network map (link-state), Bellman-Ford only knows neighbors (distance-vector).

**Q2:** What is the count-to-infinity problem?
**A2:** A problem in distance-vector routing where routers keep increasing the distance to an unreachable destination.

**Q3:** What is the main advantage of OSPF over RIP?
**A3:** OSPF is faster and more scalable because it only shares changes, not full tables. 