# 🔀 Phase 2: The Traffic Controller (Distributed Core)

**Target Pool:** 700 XP to Level Up to Level 3.
**Core Objective:** Master the messy physics of multiple machines interacting. Learn what happens when networks drop packets, clocks drift, and partitions occur.

---

## 📚 Main Quests: DDIA Integration

### 🔹 Quest 2.1: Data Duplication Strategies
*   **Source Material:** DDIA Chapter 5
*   **Core Concepts:** Single-leader, multi-leader, and leaderless replication. Handling replication lag, read-after-write consistency, and split-brain scenarios.
*   **Reward:** **+20 XP**

### 🔹 Quest 2.2: Slicing the Dataset
*   **Source Material:** DDIA Chapter 6
*   **Core Concepts:** Partitioning by key range vs. key hash. Secondary index partitioning (document-partitioned vs. term-partitioned) and rebalancing storms.
*   **Reward:** **+20 XP**

### 🔹 Quest 2.3: The Illusion of Isolation
*   **Source Material:** DDIA Chapter 7
*   **Core Concepts:** ACID vs. BASE. Isolation levels: Read Committed, Snapshot Isolation, Repeatable Read, and Serializability (Two-Phase Locking vs. SSI).
*   **Reward:** **+20 XP**

### 🔹 Quest 2.4: Realities of Distributed Despair
*   **Source Material:** DDIA Chapter 8
*   **Core Concepts:** Network faults, clock skew (NTP drift, TrueTime), process pauses (GC pauses), and Byzantine faults.
*   **Reward:** **+20 XP**

### 🔹 Quest 2.5: Reaching Agreement
*   **Source Material:** DDIA Chapter 9
*   **Core Concepts:** Linearizability, Total Order Broadcast, Distributed Transactions (2PC), Consensus algorithms (Raft/Paxos high-level concepts).
*   **Reward:** **+20 XP**

---

## 🌐 Out-of-Book Gaps: Coordination & Queues

### 🔹 Quest 2.6: Event Pipelines & Stream Mechanics
*   **Concepts:** Log-based message brokers (Kafka) vs. AMQP brokers (RabbitMQ). Processing guarantees: at-least-once, at-most-once, exactly-once delivery.
*   **Reward:** **+25 XP**

### 🔹 Quest 2.7: Distributed Locks & Tokens
*   **Concepts:** Redlock algorithm via Redis vs. CP-system state coordination via ZooKeeper/Consul leases.
*   **Reward:** **+25 XP**

---

## 🏢 Real-World Anchors (Case Studies)

### 🔹 Deep-Dive 2.1: Amazon's Dynamo Blueprint
*   **Resource:** The Amazon Dynamo Paper (2007).
*   **Focus:** Sloppy Quorums, Hinted Handoff, and Vector Clocks for conflict resolution.
*   **Reward:** **+25 XP**

### 🔹 Deep-Dive 2.2: Uber’s Schemaless Engine
*   **Resource:** Uber Engineering Blog.
*   **Focus:** How Uber structured an append-only, shardable datastore on top of raw MySQL instances.
*   **Reward:** **+25 XP**

---

## ⚔️ Phase 2 Side Quests & Boss Battle

*   **Side Quest 2.1 (Codebase):** Write a consistent hashing ring simulator with configurable virtual nodes. Track data distribution deviation across nodes. Save to `/side-quests/consistent-hashing/`. **(+45 XP)**
*   **👹 Boss Battle 2.1:** Group Whiteboard Challenge: Design a distributed unique ID generator (Twitter Snowflake clone) that generates 64-bit sortable IDs across multiple data centers without a single point of failure. **(+50 XP)**