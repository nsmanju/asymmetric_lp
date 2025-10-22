```markdown
# Asymmetric Liquidity Provision — Simplified PoC

This fork contains a simplified, documentation-first version of the asymmetric liquidity provision strategy focused on the Python PoC and developer-friendly notes.

Purpose
- Present a compact, runnable Proof-of-Concept (PoC) for the asymmetric LP strategy (DeFi LP + CeFi hedging).
- Keep Docker/CI instructions optional — the PoC runs with Python locally for quicker iteration.
- Organize useful notes into focused topic pages under `topics/`.

What this fork contains
- topics/ : architecture and integration notes, PoC quickstart, thresholds, glossary
- python/ : (original Python code; use PoC scripts provided in this repo or replace with your local PoC)
- docs and examples for running the PoC (PDF/CSV outputs)

Why omit Docker/CI here
- To lower the friction for researchers and quant engineers who want to run the PoC quickly.
- Docker/CI are still part of the upstream project; we leave them documented but not required for PoC runs.

Quickstart (local, no Docker)
1. Ensure Python 3.8+ installed.
2. Setup venv:
   python3 -m venv .venv
   source .venv/bin/activate
   pip install --upgrade pip
   pip install numpy pandas matplotlib
3. Run the PoC scripts (examples live in POC/):
   python POC/simulate_poc_annotated.py
4. Inspect generated files:
   - poc_baseline.pdf
   - poc_stressed.pdf
   - summary_baseline.csv
   - hedges_baseline.csv

Notes about deployment
- Docker and full CI/CD are intentionally left out of this simplified branch. For production-ready deployment, see the upstream repo's DEPLOY.md and docker configuration.

Contributing
- If you want to add more topic pages or example runs, edit files under topics/ and open a PR on this fork or upstream.
```
