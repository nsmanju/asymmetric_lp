```markdown
# PoC Quickstart

This document explains how to run the PoC locally and what outputs to expect.

Prereqs
- Python 3.8+
- pip, virtualenv
- (Optional) Git, to manage your fork/branch

Install
- python3 -m venv .venv
- source .venv/bin/activate
- pip install --upgrade pip
- pip install numpy pandas matplotlib

Run
- python POC/simulate_poc_annotated.py

Outputs
- poc_baseline.pdf, poc_stressed.pdf — annotated multi-page PDFs per scenario
- summary_baseline.csv, summary_stressed.csv — numeric summaries (final P&L, total fees, number of hedges)
- hedges_baseline.csv, hedges_stressed.csv — detailed executed hedges

Debugging tips
- If P&L and fees plot overlap (P&L ≈ fees), run the debug helper script:
  python POC/replot_with_difference.py
- Adjust parameters in POC/simulate_poc_annotated.py to test volatility, range width, slippage, etc.

Reintegrating with C++ CeFi
- Use produced CSVs and ZMQ schema as inputs to the C++ test harness.
- The PoC generates messages and CSV artifacts suitable for exchange simulator consumption.
```
