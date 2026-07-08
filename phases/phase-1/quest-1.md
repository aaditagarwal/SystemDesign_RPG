# 📜 Quest Briefing: Week 1 Sprint
## 📖 Main Quest 1.1: Foundations of Reliability & Scale (DDIA Chapter 1)
When reading Chapter 1, do not treat it as a passive history lesson. Focus your party's attention on these specific architectural mechanics:
- The Myth of the "Average": Senior engineers do not care about average latency (mean). You must master Percentiles (p95, p99, p99.9). Pay close attention to tail latency amplification—how a single slow backend dependency can ripple up and ruin the user experience for your entire app.
- The Twitter Fan-Out Paradox: Analyze the core case study in this chapter. Understand why Twitter had to pivot from a pure relational query approach (pull-on-demand) to a per-user timeline cache approach (push-on-write), and how they handle the hybrid "celebrity edge-case" where users have tens of millions of followers.
## 🌐 Out-of-Book Gap 1.5: The Evolution of the Wire (Application Protocols)
DDIA assumes you know how bytes move. To bridge the gap to Senior level, your party must master the exact engineering trade-offs of the modern web stack:
- **HTTP/1.1 vs. HTTP/2**: Understand Head-of-Line (HOL) Blocking. HTTP/1.1 blocks at the application layer (one request per connection at a time). HTTP/2 uses multiplexing to send multiple requests concurrently over a single TCP connection.
- **The Flaw in HTTP/2**: If a single TCP packet is dropped, the entire connection freezes while waiting for retransmission. This is TCP-level Head-of-Line Blocking.
- **HTTP/3 (QUIC)**: Understand how HTTP/3 solves this by switching from TCP to UDP using the QUIC protocol. It treats streams independently; if one stream drops a packet, the others keep flowing.
- **gRPC vs. REST**: REST relies on text-based JSON over HTTP/1.1 or HTTP/2. gRPC uses Protocol Buffers (binary serialization) over strictly HTTP/2, resulting in massive CPU and bandwidth savings for internal microservices.

# 🌐 Week 1 Specializations Resources: Application Protocols & Networking
### 🚦 HTTP/1.1 to HTTP/3 & Head-of-Line (HOL) Blocking
* [Cloudflare Learning Hub: What is HTTP/3?](https://www.cloudflare.com/learning/performance/what-is-http3/)
  * **Why read:** This is a clear overview of how HTTP/3 switches to the QUIC protocol over UDP, removing TCP's inherent head-of-line blocking while enabling seamless mobile connection migration.
* [Web Performance Calendar: Head-of-Line Blocking in Depth](https://calendar.perfplanet.com/2020/head-of-line-blocking-in-quic-and-http-3-the-details/)
  * **Why read:** This contains excellent visual breakdowns of the differences between application-level HOL blocking (HTTP/1.1) and transport-level HOL blocking (HTTP/2 over TCP), explaining exactly how HTTP/3 breaks packet processing streams apart.

### 🔌 REST vs. gRPC & Protocol Serialization
* [AWS Architecture Center: gRPC vs. REST Differences](https://aws.amazon.com/compare/the-difference-between-grpc-and-rest/)
  * **Why read:** Provides an excellent look at Entity-Oriented Design (REST) versus Service-Oriented Design (gRPC), highlighting client-server coupling and unary versus multi-directional streaming capabilities.
* [Postman Engineering Blog: gRPC vs. REST Architectural Styles](https://blog.postman.com/grpc-vs-rest/)
  * **Why read:** Covers how the `protoc` compiler automatically enforces API contracts across microservices, contrasting raw text JSON parsing overhead against binary Protocol Buffer performance.

# ⚔️ Week 1 Objectives & Deliverables
To clear this sprint and update your repository via your first weekend Pull Request, your party must complete the following:
1. **The Summary Artifact** (+20 XP per player)
- Create a file named `/phases/completions/quest-1-1-summaries.md`.
- Each player must write a 5-bullet summary detailing their key takeaway from DDIA Chapter 1, specifically explaining tail latency amplification or the Twitter fan-out paradox in their own words.
2. **The Networking Deep-Dive** (+25 XP per player)
- Create a file named `/phases/completions/networking-deep-dive.md`.
- Together or individually, map out a markdown table comparing REST (JSON) vs gRPC (Proto) across Latency, Payload Size, Stream Capabilities, and Best Use Case.
3. **The Co-op Raid Prep**: "The Twitter Breakdown" (+50 XP potential)
- Set up a 45-minute weekend call with your party. Open a digital whiteboard (Miro/Excalidraw).
- Draw the architecture for Twitter Variant A (Look up tweets on the fly).
- Draw the architecture for Twitter Variant B (In-memory fan-out home timelines).
- Screenshot your drawings and save them into your `/artifacts/` directory.

# 📈 Example Sunday PR Commit Message
When you open your PR this Sunday, use a structured commit style to keep the repo clean: `feat: week 1 completion - [Player Name] +45 XP`