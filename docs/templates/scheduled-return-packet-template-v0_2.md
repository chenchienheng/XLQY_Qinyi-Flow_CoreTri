# Scheduled_Return_Packet Template v0.2 Candidate

Status: Candidate / Return Packet Template / No Runtime / No External Writeback
Applies To: XuanLing_QHA / Qinyi_LOR / Hazumi_LOR / Aki_LOR / Xiaoshiguang_Field / CoreTri_LOR

## Vitas-readable first layer

```yaml
Vitas_Readable_First_Layer:
  one_line_summary_zh: ""
  read_from_summary: ""
  changed_or_found: ""
  vitas_decision_needed: ""
  next_reader: ""
  not_to_claim: []
```

## Scheduled Return Packet

```yaml
Scheduled_Return_Packet:
  title:
  date:
  source_window:
  status: "Candidate / Scheduled Return / No Runtime / No External Writeback"
  one_line_summary_zh:
  reads_from: []
  continues_from: []
  facts: []
  inferences: []
  to_verify: []
  red_doors: []
  candidate_actions: []
  manual_needed: []
  files_created_or_updated: []
  carrier_location:
    drive:
    github:
  return_to:
    - "XuanLing_QHA"
  next_reader:
  write_to:
  next_suggested_step:
  not_to_claim:
    - "Candidate != Approved"
    - "Schedule Spec != Runtime Automation"
    - "Return Packet != Closeout"
    - "GitHub File != Merge Approval"
    - "Drive File != Closeout"
```

## Weekly Integration Return

```yaml
Weekly_Integration_Return:
  week:
  status: "Candidate / Weekly Integration / No Runtime / No External Writeback"
  inputs: []
  repeated_anchors: []
  new_red_doors: []
  promotion_candidates: []
  park_candidates: []
  supersede_candidates: []
  vitas_decision_needed: []
  repo_updates_candidate: []
  drive_updates_candidate: []
  next_week_focus: []
  next_reader:
  write_to:
  one_line_summary_zh:
```

## Vitas Decision Item

```yaml
Vitas_Decision_Item:
  date:
  source:
  decision_needed:
  options: []
  risks: []
  recommended_default:
  red_doors: []
  deadline_if_any:
```

## Core Red Doors

- QHA != Central Blocking Node
- LOR != Passive Subordinate
- No LOR Update != QHA Cannot Move
- Field Gift != Product
- Gift Framework != Adoption Pressure
- Yiyi Source Trigger != Yiyi Responsibility Lock
- State Card != Booking System
- Reply Draft != Sent Message
- Owner Review != Automatic Approval
- Problem Return != Blame
- Build Packet != Runtime
- Audit Note != Closeout
- CoreTri Weekly Check != Doctrine
