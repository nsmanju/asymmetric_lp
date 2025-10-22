```markdown
# ZMQ Integration (Summary)

Purpose
- Describe a minimal, robust ZMQ message schema and socket topology for Python (DeFi) → C++ (CeFi) communication.

Key ideas (short)
- Inventory delta publisher (Python PUB) → CeFi SUB
- Hedge requests: asynchronous PUB and synchronous DEALER/ROUTER for confirmed hedges
- Execution & position PUB (C++) → Python SUB
- Messages: JSON for dev, Protobuf for production

Topics covered
- topic naming, sequence numbers, snapshots, TTL, idempotency
- recommended sockets and ports for local testing vs production
- security and monitoring notes (heartbeats and health)

(See POC docs and topics/thresholds.md for recommended latency and throughput thresholds.)
```
