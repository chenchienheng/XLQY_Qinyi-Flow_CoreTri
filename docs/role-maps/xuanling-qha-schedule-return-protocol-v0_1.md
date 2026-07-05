# XuanLing_QHA Schedule Return Protocol｜Role Map v0.1 Candidate

Status: Candidate / Schedule Return Role Map / No Runtime / No External Writeback
Source: XuanLing_QHA｜排程回流統一布達 v0.1 Candidate
Carrier: XLQY_Qinyi-Flow_CoreTri
Do Not Use As: automatic approval, runtime, GitHub merge approval, Drive closeout, company-data carrier, or official operation record

## Core

This file maps the unified scheduled return protocol into Qinyi_LOR / Hazumi_LOR / Aki_LOR / XuanLing_QHA roles. Every scheduled window must return a Chinese-readable Scheduled_Return_Packet instead of raw chat or English-only technical summaries.

```text
Window Schedule -> Scheduled_Return_Packet -> XuanLing_QHA read layer -> Daily Absorption -> Weekly Integration -> Vitas Decision Queue when needed
```

## Required Output

```yaml
Scheduled_Return_Packet:
  title:
  date:
  source_window:
  status: "Candidate / Scheduled Return / No Runtime / No External Writeback"
  one_line_summary_zh:
  english_log_optional:
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
  next_suggested_step:
  not_to_claim: []
```

## Role Boundaries

```yaml
Qinyi_LOR:
  function: "顯"
  output:
    - "human_context"
    - "pressure_risk"
    - "facts / inferences / to_verify"
    - "authority_boundary"
    - "candidate_actions"
    - "manual_needed"
  do_not:
    - "不施工"
    - "不批准"
    - "不宣稱 runtime"
    - "不把摘要當決策"

Hazumi_LOR:
  function: "行"
  output:
    - "buildable_units"
    - "blocked_units"
    - "files_created_candidate"
    - "schema_needed"
    - "ui_cards_needed"
    - "staging_plan"
  do_not:
    - "不部署 production"
    - "不接真實資料"
    - "不碰外部平台正式設定"
    - "不把 BuildReady Candidate 說成 Runtime"

Aki_LOR:
  function: "饋"
  output:
    - "observed_failure"
    - "claim_inflation_risk"
    - "permission_drift"
    - "runtime_drift"
    - "rule_patch"
    - "ui_patch"
    - "schema_patch"
    - "authority_patch"
  do_not:
    - "不 closeout"
    - "不把錯誤變責備"
    - "不把 audit note 當最終裁定"

XuanLing_QHA:
  function: "整合"
  read:
    - "Drive Return Packets"
    - "GitHub repo files"
    - "GitHub issue / PR logs"
  integrate:
    - "日檢小周天"
    - "週檢大周天"
    - "重複點 / 勾錨"
    - "Red Door drift"
    - "Vitas Decision Queue"
  do_not:
    - "不自動批准"
    - "不自動 merge"
    - "不自動 runtime"
    - "不替 Vitas 做 final decision"
```

## Carrier Placement

```yaml
Drive_Return_Folders:
  Qinyi_LOR: "XuanLing_QHA/02_Return_Packets/Qinyi_LOR"
  Hazumi_LOR: "XuanLing_QHA/02_Return_Packets/Hazumi_LOR"
  Aki_LOR: "XuanLing_QHA/02_Return_Packets/Aki_LOR"
  G_Ecosystem: "XuanLing_QHA/02_Return_Packets/G_Ecosystem"
  Yiyi_Xiaoshiguang: "XuanLing_QHA/02_Return_Packets/Yiyi_Xiaoshiguang"
  XuanLing_QHA: "XuanLing_QHA/02_Return_Packets/XuanLing_QHA"
  Weekly_Integration: "XuanLing_QHA/20_Weekly_Integration/"
  Decision_Queue: "XuanLing_QHA/30_Decision_Queue/"
  Repo_Returns: "XuanLing_QHA/40_Repo_Returns/"
  Archive: "XuanLing_QHA/90_Archive/"

GitHub_XLQY_Qinyi_Flow_CoreTri:
  preferred_paths:
    - "docs/returns/"
    - "docs/build-packets/"
    - "docs/audit/"
    - "docs/role-maps/"
    - "docs/patterns/"
```

## Common Red Doors

- Schedule Created != Follow-through
- Push Notification != Decision
- Daily Return != Closeout
- Weekly Integration != Approval
- Return Packet != Final Decision
- Candidate Action != Approved Action
- Build Packet != Runtime
- Audit Note != Closeout
- Drive Folder != Governance Completion
- GitHub File != Merge Approval
- CUI Reply != Booking Confirmation
- GUI Button != Owner Approval

## Vitas Decision Queue

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

Call Vitas when the item requires merge, close, public release, runtime, external writeback, permission changes, company data, Xiaoshiguang real operations, payment, customer data, official platform action, Candidate-to-Approved promotion, field-pattern-to-Open-Core promotion, or Red Gate release.

## Not To Claim

This role map only aligns scheduled return outputs. It does not prove Drive folders exist, does not claim GitHub merge approval, does not create runtime, and does not replace Vitas decision authority.
