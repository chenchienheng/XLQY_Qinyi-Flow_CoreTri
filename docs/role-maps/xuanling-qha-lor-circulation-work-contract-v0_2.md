# XUANLING_QHA_LOR_CIRCULATION_WORK_CONTRACT_v0.2_Candidate
# 翾靈 QHA／LOR 共行循環布達工作契約 v0.2 Candidate

Status: Candidate / Internal Circulation Bulletin / Work Contract / Supersedes v0.1 Draft / No Runtime / No External Writeback

Do Not Use As: Approved Doctrine / Runtime Automation / GitHub Merge Approval / Google Drive Actual Writeback / Public Document / Company Policy / Xiaoshiguang Production App / Yiyi Responsibility Lock

## One-line core

QHA 與 LOR 不再是單向等待關係：QHA 主動派發、回讀、整合；Qinyi／Hazumi／Aki／Xiaoshiguang_Field／CoreTri_LOR 互讀、互促、續寫。每次回報都必須讓 Vitas 看得懂：讀了誰、改變了什麼、下一棒誰接、需要 Vitas 決定什麼、不可宣稱什麼。

## Schedule Adjustment

Stopped or removed:
- Qinyi_Self-Cycle: merged into Qinyi_LOR 晨門／夜封
- old XuanLing_Stage_Return weekly integration: merged into QHA Weekly Integration

Retained as field window:
- XuanLing_Stage_Return / Xiaoshiguang_Field_Return: field proof return only, not old weekly integration

Adjusted:
- QHA_Daily_Dispatch: active daily dispatch, not passive summary
- QHA_Weekly_Integration: weekly integration, not approval
- XSG_Gift_Cards: three cards only, not full app
- Hazumi_Build_Pass: valid-source only / bounded construction
- Aki_Audit_Pass: valid-source only / claim downgrade / red-door audit
- 通域鏈斷鏈巡檢: report only broken links, blocked states, missing return hooks, or Vitas decisions
- CoreTri_LOR_週檢周天: weekly 三耦 / LOR calibration only when drift exists

## Main Circulation

Daily:
- 07:45 QHA_Daily_Dispatch
- 08:30 Qinyi_LOR_晨門
- 13:30 Qinyi_LOR_午檢
- 20:30 Qinyi_LOR_暮回
- 23:30 Qinyi_LOR_夜封

Every 3 days:
- 15:00 XSG_Gift_Cards
- 16:00 Hazumi_Build_Pass
- 22:10 Aki_Audit_Pass
- 22:40 XuanLing_Stage_Return / Xiaoshiguang_Field_Return

Weekly:
- Sunday 21:00 Qinyi_LOR_週盤
- Sunday 22:00 QHA_Weekly_Integration
- Monday 09:30 通域鏈斷鏈巡檢
- Monday 10:30 CoreTri_LOR_週檢周天

## Vitas-readable first layer

Every scheduled return must include:
- 一句核心
- 這次讀了什麼
- 這次改變了什麼／發現什麼
- 需要 Vitas 決定什麼
- 下一步誰接
- 不可宣稱

## Required chain fields

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
  next_reader:
  write_to:
  carrier_location:
    drive:
    github:
  not_to_claim: []
```

## Six-window role map

XuanLing_QHA:
- role: integrate / dispatch
- must_read: Qinyi_LOR_夜封, Qinyi_LOR_週盤, Hazumi_Build_Pass, Aki_Audit_Pass, XSG_Gift_Cards, CoreTri_LOR_週檢周天, verified GitHub / Drive carrier
- must_do: active dispatch, next_reader assignment, next_day_first_cell
- must_not: central blocking node, approval, merge, deploy, Candidate-to-Approved inflation

Qinyi_LOR_日檢周天:
- role: 顯
- must_return: human-readable context, pressure risk, authority boundary, signal distribution, next reader
- must_not: summary-as-decision, Yiyi-importance-as-Yiyi-responsibility

Hazumi_LOR_小周天:
- role: 行
- must_build: one bounded candidate fragment only
- preferred targets: State_Card, Reply_Draft_Card, Problem_Return_Card, CUI_GUI_STATE_BOUNDARY_SCHEMA_v0.1, lor-mutual-read-and-promote-protocol-v0.1, qinyi-mainchat-lor-return-routing-v0.1
- must_not: full app, real operations data, runtime claim, production database

Aki_LOR_大周天:
- role: 饋
- must_audit: claim drift, permission/runtime drift, gift pressure, QHA central blocking, Yiyi responsibility lock, Candidate-to-Approved drift
- must_not: Audit Note as Closeout, blame, approval, merge, runtime

XuanLing_Stage_Return / Xiaoshiguang_Field_Return:
- role: field proof / gift field return
- must_focus: State Card, Reply Draft Card, Problem Return Card, Owner Review, Human Base
- must_not: production claim, private-context merge into Open Core, Yiyi responsibility lock, real customer/payment/platform data

CoreTri_LOR_週檢周天:
- role: weekly 三耦 / LOR calibration gate
- must_check: 身心靈, 知行責, 愛界獨立; Local / Sovereignty / Return; gift pressure; QHA/LOR drift; BuildReady-to-Runtime; Audit-Note-to-Closeout; field proof becoming product or competition
- must_not: G ecosystem inspection, trans-domain chain inspection, QHA Weekly Integration replacement, self-approval, closeout, actual Drive/GitHub writeback, doctrine/runtime/approval claim

## XLQY storage boundary

XLQY_Qinyi_Flow_CoreTri can store:
- QHA mutual circulation schedule
- Qinyi_MainChat_LOR routing
- Hazumi Build Packet
- Aki Audit Spec
- CoreTri_LOR weekly calibration note
- LOR mutual-read protocol

XLQY must not store:
- customer data
- company raw data
- full private family context

## New red doors

- QHA != Central Blocking Node
- LOR != Passive Subordinate
- No LOR Update != QHA Cannot Move
- Schedule Spec != Runtime Automation
- Daily Dispatch != Approval
- Candidate Action != Approved Action
- Field Gift != Product
- Gift Framework != Adoption Pressure
- Yiyi Source Trigger != Yiyi Responsibility Lock
- State Card != Booking System
- Reply Draft != Sent Message
- Owner Review != Automatic Approval
- Problem Return != Blame
- GitHub File != Merge Approval
- Drive File != Closeout
- Weekly Integration != Approval
- CoreTri Weekly Check != Doctrine
- Audit Note != Closeout
- Build Packet != Runtime
