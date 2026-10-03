# Inference-lab

An attempt to learn Inference Engineering

# Together AI

Core requirements (all levels)

- Go, Python or Rust, with typed, tested code shipped via CI/CD
- Durable workflow orchestration: Temporal, Cadence
- Control planes that model state and reconcile it, like Kubernetes controllers/operators and custom reconciliation loops
- Event-driven systems: Kafka, NATS, SQS (not polling or cron)
- Product mindset: internal platforms or APIs used by other engineering teams

What you'd build

- A provisioning state machine: host discovery → GPU driver/CUDA bring-up → health validation → decommission/RMA
- A declarative self-service API: one call to stand up, scale or tear down an inference cluster
- Self-healing: detect bad nodes, drain them, repair, return them to the pool
- Reliability work: idempotency, retries, rollback, drift detection

Nice to have

- Bare-metal provisioning: PXE/iPXE, Redfish/IPMI, BMC
- Networking: VLANs, BGP
- GPU stack: NCCL, CUDA, InfiniBand/RoCE
- Systems programming in Rust or Go
