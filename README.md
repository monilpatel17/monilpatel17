# Monil Patel

Backend and systems engineer, CS graduate from Arizona State University (May 2026, GPA 3.78).
I work mostly in Rust, Go, C++, and Python, and I'm most interested in distributed systems,
storage engines, and the networking layer.

Previously built payments infrastructure at FinPay and graph-backed APIs at Grey Box.

---

## Systems built from scratch

**[Raft Leader Election & Membership](https://github.com/monilpatel17/Raft-Leader-Election-Membership)** · Go
Leader election and cluster membership changes — randomized election timeouts drawn from
[150ms, 300ms), one-vote-per-term enforcement, and split-vote resolution by backoff. Failover on a
5-node cluster measures p50 173ms / p99 207ms (n=30), against a theoretical floor of 100ms. Seeded
chaos testing across 24 seeds × 12 injected faults each audited ~14,800 invariant samples with zero
split-brain events; a partitioned minority provably elects nobody, and the test asserts it.

**[XDP Rate Limiter & L4 Load Balancer](https://github.com/monilpatel17/XDP-Rate-Limiter-L4-Load-Balancer)** · C (eBPF/XDP)
Per-source token-bucket rate limiting and layer-4 load balancing in the kernel datapath, before
packets reach the network stack. Rendezvous hashing over a 65537-slot table holds worst-case
per-backend deviation to 0.0107% at 10 backends; removing a backend moves 10.191% of slots against
a 9.999% floor, of which only 0.192% belonged to flows that weren't on it. 2,055 assertions on table
properties plus 14 token-bucket accuracy checks, including 1,000-hour idle overflow and
backwards-clock cases. Raw throughput is deliberately unmeasured and documented as such — the
loader refuses to fall back to skb-mode silently, so generic-mode results can't be mistaken for
native ones.

**[Write-Ahead Log](https://github.com/monilpatel17/Write-ahead-log)** · C++
Durable append-only log with crash-consistent recovery and CRC-checked records. Group commit lifts
throughput from 9,056 appends/s (fsync per write, p50 104µs) to 701,720/s at p50 0.50µs — 77.5× —
and the write-up works through why a 10ms time-based window *loses* to N=100 batching at 64 KiB
records. Validated by 500 crash-injection cycles per policy that truncate or bit-flip the log past
the durability point: 0 committed records lost across 320,000+ commits, with 562 genuinely torn
frames detected and rejected.

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

## Languages and Tools

**Languages**

<img src="https://skillicons.dev/icons?i=rust,go,c,cpp,py,java,ts" />

**Data & Infrastructure**

<img src="https://skillicons.dev/icons?i=postgres,mongodb,redis,kafka,docker,kubernetes,terraform,gcp,aws,linux" />

Also working with: Neo4j · Apache Beam / Dataflow · BigQuery · eBPF/XDP · gRPC · Tokio · Spring Boot · FastAPI


## Connect With Me

<a href="https://linkedin.com/in/YOUR-HANDLE"><img src="https://skillicons.dev/icons?i=linkedin" /></a>
&nbsp;
<a href="https://personal-website-chi-two-65.vercel.app"><img src="https://skillicons.dev/icons?i=vercel" /></a>

monilapatel1989@gmail.com
