```markdown
# Latency & Throughput Thresholds (Practical Guide)

When to keep Python vs move to C++/Rust:
- Decision cadence:
  - Minutes → Python OK
  - Sub-minute, >1s → Python acceptable
  - Sub-second → consider C++/Rust
- End-to-end signal-to-fill:
  - Soft: <200 ms (Python OK)
  - Moderate: 50–200 ms (prefer C++ for consistency)
  - Strict: <50 ms (C++/Rust)
- Orders-per-second (OPS):
  - <100 OPS → Python
  - 100–500 OPS → optimize or mix
  - >500 OPS → C++/Rust

Operational suggestions
- Always collect P50/P90/P99 and P999 latency metrics
- Use binary serialization (Protobuf) when messaging >500 msgs/s
- Start with JSON+ZMQ for development and move to Protobuf for production
```
