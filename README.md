# Monil Patel

Backend and systems engineer, CS graduate from Arizona State University (May 2026, GPA 3.78).
I work mostly in Rust, Go, C++, and Python, and I'm most interested in distributed systems,
storage engines, and the networking layer.

Previously built payments infrastructure at FinPay and graph-backed APIs at Grey Box.
**Currently looking for a full-time backend or infrastructure role.**

---

## Systems built from scratch

**[Raft Leader Election & Membership](https://github.com/monilpatel17/Raft-Leader-Election-Membership)** · Go
Implementation of Raft leader election and cluster membership changes — [terms, election timeouts,
split-vote handling, and joint consensus for reconfiguration]. Verified with [N] tests covering
[partition / stale-leader / concurrent-election] scenarios.

**[XDP Rate Limiter & L4 Load Balancer](https://github.com/monilpatel17/XDP-Rate-Limiter-L4-Load-Balancer)** · C (eBPF/XDP)
Packet-level rate limiting and layer-4 load balancing running in the kernel datapath via XDP,
before packets reach the network stack. [Token-bucket limiting with per-source state in BPF maps;
consistent-hash backend selection.] Sustained [X] pps at [Y] on [hardware].

**[Write-Ahead Log](https://github.com/monilpatel17/Write-ahead-log)** · C++
Durable append-only log with [crash-consistent recovery, CRC-checked records, and segment rotation].
Correctness validated by [crash-injection / fsync-fault tests]. [Throughput number.]

**[Redis-Like In-Memory Key-Value Store](https://github.com/monilpatel17/Redis-Rust)** · Rust, Tokio
TCP key-value server on the Tokio async runtime with RESP protocol framing and a task-per-connection
model over a non-blocking event loop. Sustains ~30,000 ops/s (42,000 under 10 concurrent clients)
at ~35µs average latency over 50,000 operations on an Apple M2.

---

## Production-grade cloud work

**[Serverless File Processing on GCP](https://github.com/monilpatel17/Serverless-File-Processing-on-GCP)** · Python, Cloud Run, Pub/Sub, Firestore, Terraform
Event-driven CSV pipeline with streaming file processing and batched writes. Deterministic SHA-256
record IDs make at-least-once reprocessing idempotent by construction. Transient and permanent
failures are classified onto platform retry semantics with dead-lettering, and invalid rows are
quarantined against a configurable reject threshold. 36 Terraform resources with least-privilege
IAM; 178 tests at 98% coverage, fully offline.

**[Real-Time Event Analytics Pipeline](https://github.com/monilpatel17/Real-Time-Event-Analytics-Pipeline)** · Apache Beam, Dataflow, BigQuery
Streaming pipeline computing per-device rolling averages over 60s fixed windows, with watermark-based
120s allowed lateness so out-of-order readings re-fire their window instead of being dropped.
Anomaly detection combines a fixed threshold with an adaptive 3σ check against each device's own
window — 97–100% recall and 93–97% precision across five seeds against injected ground truth.
42 offline tests, including TestStream cases for on-time, late, and beyond-lateness panes.

---

## Experience

**Software Engineer Intern — Grey Box** (Jan–May 2026)
Built the FastAPI middleware between the front end and a Neo4j graph database serving translated
drug names across 100+ languages. Migrated the store from SQL to Neo4j, modeling medical terms as
a graph so related drugs and translations resolve in one traversal instead of multiple joins —
~30% faster lookups.

**Software Development Engineer Intern — FinPay** (Jul–Dec 2025)
Retry logic and idempotency controls for Stripe payment and refund webhooks in Java/Spring Boot,
in a system processing $5M+ in transactions for 100k+ customers. Cut dashboard load time from 4–5s
to under 1s via compound indexes and refactored MongoDB aggregation pipelines.

**Technology Consultant — Arizona State University** (May 2024–Jun 2025)
Flask/Oracle REST API for class scheduling serving 120k+ students and 4,500+ faculty, handling
50k+ requests at peak registration.

---

## Tools

**Languages:** Rust, Go, C, C++, Python, Java, SQL
**Systems:** TCP/IP, eBPF/XDP, async runtimes (Tokio), gRPC, concurrency
**Data:** PostgreSQL, MongoDB, Neo4j, Redis, BigQuery, Apache Beam
**Infra:** Docker, Kubernetes, Terraform, GCP (Cloud Run, Pub/Sub, Dataflow), AWS (ECS)

---

[Portfolio](https://personal-website-chi-two-65.vercel.app) · [LinkedIn](https://linkedin.com/in/YOUR-HANDLE) · mpate207@asu.edu
