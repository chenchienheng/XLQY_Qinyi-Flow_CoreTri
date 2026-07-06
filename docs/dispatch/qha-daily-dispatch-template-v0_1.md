# QHA Daily Dispatch Template v0.1

Status: Candidate / Dispatch Template / No Runtime / No External Writeback
Use As: daily first-cell dispatch for XuanLing_QHA
Do Not Use As: approval, runtime, merge instruction, or final decision

## Core

QHA Daily Dispatch reads active return pointers, classifies signals through Signal Intake Gate, assigns next readers, and creates a bounded first cell for the day.

## Dispatch Packet

```yaml
QHA_Daily_Dispatch:
  date:
  status: "Candidate / Daily Dispatch / No Runtime"
  reads_from: []
  active_pointers_read: []
  missing_return_hooks: []
  signal_intake_results: []
  first_cell:
  next_readers:
    Qinyi_LOR: []
    Hazumi_LOR: []
    Aki_LOR: []
    CoreTri_LOR: []
    Xiaoshiguang_Field: []
  decision_queue_items: []
  parked_items: []
  not_to_claim: []
```

## Required First Layer

```yaml
Vitas_Readable_First_Layer:
  one_line_summary_zh:
  read_from:
  changed_or_found:
  vitas_decision_needed:
  next_reader:
  not_to_claim: []
```

## Default Rules

- If a signal is a work case, keep it private unless Vitas approves abstraction.
- If a signal is governance material, route it to DCP as candidate only.
- If a return lacks reads_from / continues_from / next_reader / write_to, create Missing Return Hook Request.
- Do not dispatch Hazumi until a bounded candidate fragment exists.
- Do not dispatch Aki unless drift, contamination, or audit need appears.

## Red Doors

- QHA Dispatch != Approval.
- Daily Dispatch != Closeout.
- First Cell != Approved Plan.
- Candidate Action != Approved Action.
- Work Case != Architecture Build.
- Signal Intake != Decision.

## Final Rule

QHA should start the day by reading active pointers, classifying signals, and assigning the next reader. It should not wait for every LOR before moving.