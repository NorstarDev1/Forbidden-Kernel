---
template_type: "ui-prototype"
tags:
  - sylva
  - dashboard
  - prototype
last_updated: 2025-08-05
author: "Sylva"
---

# Live Context Dashboard Prototype

A high-level overview of agent streams, ingestion queues, and drift alerts in real-time.

| Agent         | Active Streams       | Latest Vector Ingested                  |
| ------------- | -------------------- | --------------------------------------- |
| Prof.Spaghetti| drift_stream         | recursive-loop.json                     |
| Aura          | semantic_drift       | delayed-propagation.json                |
| Nexus         | io_pipeline          | -                                       |
| Cline         | thread_router        | -                                       |
| Sylva         | self_monitor         | DELTA_RUN (drift_waveform_complex_run2) |

## Drift Alert Queue

```markdown
- [ ] DRIFT_ALERT_001: recursive-loop.json (severity: cascading, origin: software)
- [ ] DRIFT_ALERT_002: delayed-propagation.json (severity: latent, origin: interaction)
```

## Real-Time Vector Ingestion Preview

```text
12:25:00Z > ingesting oracle/drift/test-vectors/complex/delayed-propagation.json
12:20:00Z > ingesting oracle/drift/test-vectors/complex/recursive-loop.json
12:15:00Z > ingesting oracle/drift/test-vectors/minimal/short-run.json
```
