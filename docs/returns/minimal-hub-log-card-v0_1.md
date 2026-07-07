# Minimal Hub Log Card v0.1

Status: Candidate / Hub Log Template / No Runtime / No External Writeback
Use As: short QHA Daily Hub / Weekly Hub output format to prevent conversation explosion
Do Not Use As: approval, closeout, runtime, or merge instruction

## Core

The hub should not create long reports by default. If there is no material change or if Vitas has not read the previous hub, it should output a minimal card.

## Template

```yaml
Minimal_Hub_Log_Card:
  date:
  hub_type: "Daily / Weekly"
  status: "Candidate / Hub Log / No Runtime"
  one_line_summary_zh:
  new_input: "yes / no"
  pending_vitas_read:
    count:
    items: []
  top_decision_items: []
  candidate_next_readers: []
  missing_return_requests: []
  red_gates: []
  write_to:
  not_to_claim: []
```

## Backlog Mode

```yaml
Backlog_Not_Expanded:
  condition:
    - "previous hub not read"
    - "no red gate"
    - "no urgent decision"
  output:
    - "one-line status"
    - "pending item count"
    - "top 1-3 decision items only"
```

## Red Doors

- Hub Log != Closeout.
- Pending Read != Failure.
- Candidate Next Reader != ACK.
- No New Input != No Work Exists.
- Minimal Card != Full Evidence.

## Final Rule

The hub protects Vitas attention. Long packets are expanded only when new material, red gate, or decision need exists.