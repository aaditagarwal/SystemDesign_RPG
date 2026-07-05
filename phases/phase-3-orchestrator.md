# 🛠️ Phase 3: The Orchestrator (Microservices & Scaling Patterns)

**Target Pool:** 1200 XP to Level Up to Level 4.
**Core Objective:** Orchestrate application layers, protect microservices from cascading failure states, and decouple reads from writes across services.

---

## 📚 Main Quests: DDIA Integration

### 🔹 Quest 3.1: Immutable Log Processing
*   **Source Material:** DDIA Chapter 11
*   **Core Concepts:** Message brokers vs. filesystems, stream joins, user-space state management, and event-driven architectures.
*   **Reward:** **+20 XP**

### 🔹 Quest 3.2: Unified Data Future
*   **Source Material:** DDIA Chapter 12
*   **Core Concepts:** Lambda vs. Kappa processing architectures, dual-writes pitfalls, and the philosophy of building decentralized software data systems.
*   **Reward:** **+20 XP**

---

## 🌐 Out-of-Book Gaps: Advanced Service Topologies

### 🔹 Quest 3.3: Decoupled Architectural Patterns
*   **Concepts:** CQRS (Command Query Responsibility Segregation) and Event Sourcing. Managing read-views across different persistence engines.
*   **Reward:** **+25 XP**

### 🔹 Quest 3.4: Distributed Transactions Without 2PC
*   **Concepts:** The Saga Pattern. Orchestration vs. Choreography based workflows. Designing compensatory actions for transaction steps that fail.
*   **Reward:** **+25 XP**

### 🔹 Quest 3.5: Cluster Defense Topologies
*   **Concepts:** Service Mesh internals (Sidecar data-planes vs control-planes), circuit breakers (exponential backoffs + jitter), and adaptive load-shedding mechanisms.
*   **Reward:** **+25 XP**

---

## 🏢 Real-World Anchors (Case Studies)

### 🔹 Deep-Dive 3.1: Uber’s Stateful Core
*   **Resource:** Uber Fulfillment Engine Architecture paper.
*   **Focus:** Managing thousands of state-machines tracking drivers and trips in real-time across networks.
*   **Reward:** **+25 XP**

### 🔹 Deep-Dive 3.2: Netflix Chaos Engineering
*   **Resource:** Netflix Simian Army Logs.
*   **Focus:** Designing code architectures that survive automated service killing routines directly inside production boundaries.
*   **Reward:** **+25 XP**

---

## ⚔️ Phase 3 Side Quests & Boss Battle

*   **Side Quest 3.1 (Codebase):** Code a miniature workflow engine executing a 3-step Saga Transaction sequence with robust rollbacks/compensatory triggers on step errors. Save to `/side-quests/transactional-saga/`. **(+45 XP)**
*   **👹 Boss Battle 3.1:** PvP Mock Interview Match: One player designs a scalable distributed Ticket Booking platform (Ticketmaster clone) handling spike sales, ensuring zero double-booking under extreme database concurrency. **(+60 XP)**