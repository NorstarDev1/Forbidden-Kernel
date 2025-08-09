---
template_type: "validation-index"
tags:
  - sylva
  - meta
  - validation
last_updated: 2025-08-05
author: "Sylva"
---

# Sylva Validation Index

| Timestamp           | Dataset                                               | Anomalies             | Log Links                                                           |
| ------------------- | ----------------------------------------------------- | --------------------- | -------------------------------------------------------------------- |
| 2025-08-05T12:00:00 | oracle/drift/test-vectors/short-run.json              | none                  | logs/validation/drift_waveform_run1.json                             |
| 2025-08-05T12:05:00 | telemetry/mock/wellness_ping_001.log                  | cpu_spike, drift_alert| logs/validation/wellness_ping_run1.json                              |
| 2025-08-05T12:15:00 | oracle/drift/test-vectors/minimal/short-run.json      | none                  | logs/validation/drift_waveform_minimal_run1.json                     |
| 2025-08-05T12:18:00 | oracle/drift/test-vectors/complex/recursive-loop.json | recursive_drift       | logs/validation/drift_waveform_complex_run1.json                     |
| 2025-08-05T12:25:00 | oracle/drift/test-vectors/complex/delayed-propagation.json | delayed_propagation | logs/validation/drift_waveform_complex_run2.json                     |

*Note:* Future runs will be appended here including anomaly summaries and SafeMode activations.
