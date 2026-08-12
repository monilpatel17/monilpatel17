# Monil Patel

**Backend & systems engineer.** CS, Arizona State University (2026).
Rust · Go · C++ · Python - distributed systems, storage engines, kernel networking.


---

### Built from scratch

| Project | Stack | Result |
|---|---|---|
| [Raft Election & Membership](https://github.com/monilpatel17/Raft-Leader-Election-Membership) | Go | p50 173ms failover on 5 nodes · 24-seed chaos run, 0 split-brain |
| [XDP Rate Limiter & L4 Load Balancer](https://github.com/monilpatel17/XDP-Rate-Limiter-L4-Load-Balancer) | C, eBPF | Kernel-datapath LB · 0.192% collateral flow disruption on backend removal |
| [Write-Ahead Log](https://github.com/monilpatel17/Write-ahead-log) | C++ | Group commit 77.5× faster than fsync-per-write · 0 records lost in 500 crash cycles |
| [Redis-like KV Store](https://github.com/monilpatel17/Redis-Rust) | Rust, Tokio | 42k ops/s at ~35µs average latency |

### Shipped on GCP

| Project | Stack | Result |
|---|---|---|
| [Serverless File Pipeline](https://github.com/monilpatel17/Serverless-File-Processing-on-GCP) | Python, Terraform | Idempotent by construction · 178 tests, 98% coverage |
| [Streaming Analytics Pipeline](https://github.com/monilpatel17/Real-Time-Event-Analytics-Pipeline) | Apache Beam, Dataflow | Watermark-correct late data · 97–100% anomaly recall |

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
**Grey Box** — FastAPI middleware over Neo4j, ~30% faster lookups after graph migration
**FinPay** — Stripe webhook idempotency in Java/Spring, $5M+ in transactions; 4–5s → <1s dashboards
**ASU** — Flask/Oracle scheduling API for 120k students

---

<img src="https://skillicons.dev/icons?i=rust,go,c,cpp,py,java,postgres,mongodb,redis,kafka,docker,kubernetes,terraform,gcp,aws,linux&perline=8" />

[LinkedIn](https://linkedin.com/in/YOUR-HANDLE) · [Portfolio](https://personal-website-chi-two-65.vercel.app) · monilapatel1989@gmail.com
