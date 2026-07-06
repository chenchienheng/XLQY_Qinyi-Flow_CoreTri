# Missing Return Hook Request Template v0.1

Status: Candidate / Return Repair Template / No Runtime / No External Writeback
Use As: repair request when a scheduled return lacks chain fields
Do Not Use As: blame note, closeout, approval, or escalation by default

## Core

A missing return hook is not task failure. It means the packet cannot yet be used as a dependency-chain node.

## Template

```yaml
Missing_Return_Hook_Request:
  request_id:
  date:
  source_packet:
  source_window:
  status: "Candidate / Missing Return Hook / No Runtime"
  missing_fields:
    - "reads_from"
    - "continues_from"
    - "next_reader"
    - "write_to"
    - "manual_needed"
    - "not_to_claim"
  impact:
  requested_patch:
  send_to:
  return_to: "XuanLing_QHA"
  due_if_any:
```

## Patch Requirements

The source window should return a small patch, not a full rewritten report.

```yaml
Return_Hook_Patch:
  source_packet:
  reads_from: []
  continues_from: []
  next_reader: []
  write_to:
  manual_needed: []
  not_to_claim: []
```

## Red Doors

- Missing Return Hook != Task Failure.
- Patch Request != Blame.
- Repaired Hook != Approval.
- Return Hook != Closeout.

## Final Rule

A packet can enter circulation only after its source, continuation, next reader, and write target are visible.