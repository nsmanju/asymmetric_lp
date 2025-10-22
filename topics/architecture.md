```markdown
# Architecture (Simplified view)

Overview
- Python DeFi component (strategy + PoC): handles Uniswap V3 LP logic, backtests, and publishes inventory deltas.
- C++ CeFi component (execution): high-performance execution, market servers, and position tracking (kept out of PoC to reduce complexity).
- Messaging: use ZMQ in production for low-latency signaling; PoC can simulate this locally.

Components in this fork
- PoC/Python: self-contained simulation (price path, LP range, fees, hedging) — ideal for research.
- Topics pages: detailed notes for integration, thresholds, and operational practices.
- Optional: simple ZMQ message schema included in topics for future integration.

Design choices for simplified PoC
- Focus on replicable numeric experiments (CSV + PDF outputs).
- Keep execution/hardening in C++ out of scope for rapid iteration.
- Make Docker optional — instructions included for both Docker-based and local Python runs.
```
