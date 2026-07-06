# Night Seal Timestamp Normalization v0.1

Status: Candidate / Schedule Hygiene / No Runtime / No External Writeback
Use As: timestamp interpretation rule for Qinyi_LOR night seal and QHA daily dispatch handoff
Do Not Use As: proof of actual schedule execution, approval, closeout, or external writeback

## Core

Night seal packets can show multiple times. This does not automatically mean a schedule error. It can mean different timestamp layers.

## Timestamp Layers

```yaml
Timestamp_Layers:
  schedule_run_time:
    meaning: "when the scheduled task was intended to run"
  generated_at:
    meaning: "when the packet text was produced"
  filed_at:
    meaning: "when the packet was saved to Drive / GitHub"
  modified_at:
    meaning: "when the carrier document was edited"
  qha_read_at:
    meaning: "when XuanLing_QHA read the packet"
  vitas_seen_at:
    meaning: "when Vitas saw or approved the packet"
```

## Interpretation Rule

```yaml
If_Two_Times_Appear:
  first_check:
    - "are they different timestamp layers?"
    - "are there duplicate files?"
    - "is one a draft and one a filed packet?"
    - "is one a schedule run and one an edit time?"
  do_not_assume:
    - "schedule error"
    - "duplicate valid return"
    - "closeout"
```

## Required Future Header

Every night seal should include:

```yaml
Night_Seal_Header:
  schedule_run_time:
  generated_at:
  filed_at:
  qha_read_at:
  source_window:
  canonical_packet_id:
  supersedes: []
  retention_class:
```

## Red Doors

- Two Timestamps != Schedule Error by default.
- Modified Time != Generated Time.
- Filed Packet != Approved Packet.
- Night Seal != Closeout.
- Duplicate Draft != Duplicate Canonical Return.

## Final Rule

Time ambiguity should be normalized into timestamp layers before QHA treats it as a schedule conflict or missing return hook.