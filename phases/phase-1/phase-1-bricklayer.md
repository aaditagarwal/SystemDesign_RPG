# 🪵 Phase 1: The Bricklayer (Foundations)

**Target Pool:** 300 XP to Level Up to Level 2.
**Core Objective:** Understand how a single node processes data, how data is serialized onto wires, and how incoming external traffic routes through boundaries safely.

---

## 📚 Main Quests: DDIA Integration

### 🔹 Quest 1.1: Foundations of Reliability & Scale
*   **Source Material:** DDIA Chapter 1
*   **Core Concepts:** SLAs vs. SLOs, Latency vs. Throughput, Percentiles (p99, p99.9) for system behavior analysis.
*   **Reward:** **+20 XP**

### 🔹 Quest 1.2: The Data Shape Debate
*   **Source Material:** DDIA Chapter 2
*   **Core Concepts:** Relational vs. Document vs. Graph models. Deciding schema-on-write vs. schema-on-read.
*   **Reward:** **+20 XP**

### 🔹 Quest 1.3: Under the Hood of Storage Engines
*   **Source Material:** DDIA Chapter 3
*   **Core Concepts:** Log-Structured Merge-Trees (LSM-Trees) vs. Balanced Trees (B-Trees). Write-Ahead Logs (WAL) and SSTables.
*   **Reward:** **+20 XP**

### 🔹 Quest 1.4: Serialization & Over-the-Wire Formats
*   **Source Material:** DDIA Chapter 4
*   **Core Concepts:** Binary encoding schemas. Protocol Buffers, Avro, and JSON backward/forward compatibility.
*   **Reward:** **+20 XP**

---

## 🌐 Out-of-Book Gaps: Networking & Edge Architecture

### 🔹 Quest 1.5: Application Protocols & Streaming
*   **Concepts:** HTTP/1.1 head-of-line blocking vs HTTP/2 multiplexing vs HTTP/3 QUIC connection migration. gRPC vs REST API layouts, and persistent WebSockets.
*   **Reward:** **+25 XP**

### 🔹 Quest 1.6: Boundary Traffic Management
*   **Concepts:** Layer 4 (TCP/IP routing) vs. Layer 7 (Application filtering) Load Balancing, Anycast network routing, CDN edge caches.
*   **Reward:** **+25 XP**

---

## 🏢 Real-World Anchors (Case Studies)

### 🔹 Deep-Dive 1.1: Facebook’s Scaled Caching Tier
*   **Resource:** Facebook's scaling Memcached Paper.
*   **Focus:** Managing lease mechanisms to fix thundering herds and stale data overrides.
*   **Reward:** **+25 XP**

### 🔹 Deep-Dive 1.2: Netflix Edge Routing Engine
*   **Resource:** Zuul Gateway Engineering Logs.
*   **Focus:** Dynamic filter loading, crypto offloading, and global load shedding.
*   **Reward:** **+25 XP**

---

## ⚔️ Phase 1 Side Quests & Boss Battle

*   **Side Quest 1.1 (Codebase):** Implement a fully functional token-bucket rate limiter locally in your language of choice. Code must go into `/side-quests/rate-limiter/`. **(+45 XP)**
*   **👹 Boss Battle 1.1:** Build an end-to-end architectural blueprint of a scalable distributed URL Shortener (Bit.ly clone) handling 10,000 write ops/sec. Must defend database choice, caching strategy, and custom base-62 ID generation algorithms during a Co-op whiteboard review. **(+50 XP)**