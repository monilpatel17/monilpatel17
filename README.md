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

### Experience

**Grey Box** — FastAPI middleware over Neo4j, ~30% faster lookups after graph migration
**FinPay** — Stripe webhook idempotency in Java/Spring, $5M+ in transactions; 4–5s → <1s dashboards
**ASU** — Flask/Oracle scheduling API for 120k students

---

<img src="https://skillicons.dev/icons?i=rust,go,c,cpp,py,java,postgres,mongodb,redis,kafka,docker,kubernetes,terraform,gcp,aws,linux&perline=8" />

[LinkedIn](https://linkedin.com/in/YOUR-HANDLE) · [Portfolio](https://personal-website-chi-two-65.vercel.app) · monilapatel1989@gmail.com
