# Vitas LiveIntake Window Classification and QHA Return v0.1

Status: Candidate / MainChat Intake / Human-Aligned Source Window / No Runtime / No External Writeback
Use As: source-window classification for XuanLing_QHA, QHA Daily Dispatch, Qinyi_LOR, Hazumi_LOR, Aki_LOR, CoreTri_LOR, and Xiaoshiguang Field Return
Do Not Use As: Qinyi_LOR body, schedule node, approved doctrine, GitHub/Drive actual writeback proof, runtime, closeout, or replacement for Vitas final decision

## Core

Vitas_LiveIntake is not Qinyi_LOR and not a scheduled return window. It is the immediate source window for Vitas live thoughts, corrections, rejections, framing adjustments, and candidate nutrients. QHA must read it as Source / Intake / Manual Alignment before routing to Qinyi, Hazumi, Aki, CoreTri, Xiaoshiguang Field, or Vitas Decision Queue.

## Classification

```yaml
Window_Classification:
  canonical_name: "Vitas_LiveIntake"
  zh_name: "Vitas 即時隨想入口"
  aliases:
    - "Vitas_MainChat_Intake"
    - "主談人工對齊與候選養料入口"
    - "隨想隨聊源頭窗"
  status:
    - "Live Intake"
    - "Candidate Source"
    - "Manual Alignment"
    - "No Runtime"
    - "No External Writeback"
  authority: "Vitas retains sovereignty"
```

## Is / Is Not

```yaml
Is:
  - "raw source signal entrance"
  - "manual context alignment window"
  - "candidate nutrient generator"
  - "work contract draft source"
  - "red-door patch source"
  - "schedule correction draft source"
  - "field reframing source"

Not:
  - "Qinyi_LOR"
  - "QHA Daily Dispatch"
  - "Qinyi scheduled return"
  - "Hazumi Build Pass"
  - "Aki Audit Pass"
  - "CoreTri weekly cycle"
  - "GitHub / Drive actual storage proof"
  - "runtime automation"
```

## Difference From Qinyi_LOR

```yaml
Difference:
  Vitas_LiveIntake:
    nature: "raw intake"
    timing: "immediate / live / manual alignment"
    outputs:
      - "Candidate Intake"
      - "Work Contract Draft"
      - "Red Door Patch"
      - "Schedule Correction"
      - "Field Framing"
      - "Handoff Material"
  Qinyi_LOR:
    nature: "scheduled human-readable return node"
    timing: "morning / midday / evening / night seal / weekly"
    outputs:
      - "Vitas-readable Scheduled Return Packet"
      - "Human Context"
      - "Pressure Risk"
      - "Authority Boundary"
      - "Next Reader"
      - "Write To"
```

## Required Live Intake Field

```yaml
live_intake_source:
  source_window: "Vitas_LiveIntake"
  intake_type:
    - "隨想"
    - "修正"
    - "退件"
    - "契約草稿"
    - "排程修正"
    - "場域重新定位"
  packaged: false
  requires_qinyi_lor_read: false
  requires_hazumi_build: false
  requires_aki_audit: false
  requires_coretri_check: false
  requires_vitas_decision: false
```

## Dispatch Rules

```yaml
QHA_Dispatch_Rules:
  if_intake_is_chat_only:
    action: "keep_as_context"
  if_intake_contains_red_door_patch:
    next_reader: "Aki_LOR"
  if_intake_contains_buildable_fragment:
    next_reader: "Hazumi_LOR"
  if_intake_contains_human_pressure_or_wording_issue:
    next_reader: "Qinyi_LOR"
  if_intake_contains_core_structure_or_lor_drift:
    next_reader: "CoreTri_LOR"
  if_intake_contains_xiaoshiguang_field_reframing:
    next_reader: "Xiaoshiguang_Field_Return"
  if_intake_requires_approval_or_external_writeback:
    next_reader: "Vitas Decision Queue"
```

## Red Doors

- Live Intake != Scheduled Return.
- MainChat Signal != Qinyi_LOR Packet.
- Raw Thought != Candidate Action.
- Candidate Pack != Approved Decision.
- Manual Alignment != External Writeback.
- Schedule Patch Draft != Schedule Governance Complete.
- Vitas Live Correction != Doctrine.
- Conversation Output != GitHub / Drive File.

## Final Rule

QHA must treat Vitas_LiveIntake as source material requiring routing. It becomes part of the circulation only after QHA classification, next-reader assignment, and return packet packaging.