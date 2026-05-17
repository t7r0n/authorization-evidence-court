# Prior Authorization Evidence Court

A local healthcare workflow prototype for assembling synthetic prior-authorization evidence packs and validating claim support.

## Features

- Synthetic policy, clinical, and authorization-case fixtures with no PHI.
- Evidence sufficiency checks for denial risk, missing documents, and policy alignment.
- Verifier-backed decision reports and an offline review dashboard.

## Run Locally

```bash
uv sync
uv run app init-demo
uv run app ingest fixtures/
uv run app analyze
uv run app verify
uv run app dashboard
uv run app benchmark
uv run app export-demo-pack
uv run pytest -q
uv run ruff check .
```

## Outputs

- `outputs/dashboard.html`
- `outputs/decision_report.md`
- `outputs/evidence_graph.mmd`
- `outputs/risk_or_quality_report.csv`
- `outputs/benchmark.md`
- `outputs/demo_pack.md`

## Data Policy

This project runs fully locally on deterministic synthetic fixtures. It does not require external APIs, credentials, private datasets, network access, or production systems.
