---
template_type: "drift-signature"
tags:
  - sylva
  - drift
  - classification
created_by: "Sylva"
created_date: 2025-08-05
last_updated: 2025-08-05
---

# Drift Signature Categories

| Category           | Description                                            | Example Condition      | Origin Type        | Severity Index   | Impact Scope      |
| ------------------ | ------------------------------------------------------ | ---------------------- | ------------------ | ---------------- | ----------------- |
| minimal            | Minor syntactic or semantic variation within tolerance | drift delta <= 0.002   | software           | latent           | local             |
| recursive          | Amplified drift from recursive or looped sequences     | drift delta > 0.005    | software           | cascading        | peer-linked       |
| emotional_violation| Emotional sentiment shift beyond normal parameters     | sentiment delta > 0.2  | interaction        | critical         | global            |
| latency_spike      | Significant latency increase indicating performance stress | latency delta > 10 ms | hardware           | critical         | local             |
| consensus_break    | Divergence in multi-agent witness validations          | witness disagreement   | unknown            | critical         | global            |

Use these categories to tag anomalies in validation logs and train CHRONOS for signature recognition.
