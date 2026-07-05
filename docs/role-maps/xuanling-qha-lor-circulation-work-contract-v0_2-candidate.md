# XuanLing QHA / LOR Circulation Role Map v0.2 Candidate

Status: Candidate / Internal Circulation Role Map / Work Contract Mirror / No Runtime / No External Writeback
Source: XUANLING_QHA_LOR_CIRCULATION_WORK_CONTRACT_v0.2_Candidate
Carrier: XLQY_Qinyi-Flow_CoreTri
Do Not Use As: Approved Doctrine, Runtime Automation, GitHub Merge Approval, Drive Closeout, Public Document, Company Policy, Xiaoshiguang Production App, or Yiyi Responsibility Lock

## Core

QHA and LOR are no longer one-way wait chains. QHA must dispatch, read back, and integrate. Qinyi / Hazumi / Aki / Xiaoshiguang_Field / CoreTri_LOR must mutually read, promote, and continue. Every return must answer: who was read, what changed, who receives the next baton, what Vitas must decide, and what must not be claimed.

## Mutual Circulation

```text
Qinyi 顯化 -> QHA 派發 -> Hazumi 施工 -> Aki 校驗 -> Xiaoshiguang 場域驗證 -> CoreTri_LOR 週級三耦校準 -> QHA 週整合 -> Vitas 裁定
```

## Main Schedule Map

```yaml
Daily:
  "07:45": "QHA_Daily_Dispatch"
  "08:30": "Qinyi_LOR_晨門"
  "13:30": "Qinyi_LOR_午檢"
  "20:30": "Qinyi_LOR_暮回"
  "23:30": "Qinyi_LOR_夜封"
Every_3_Days:
  "15:00": "XSG_Gift_Cards"
  "16:00": "Hazumi_Build_Pass"
  "22:10": "Aki_Audit_Pass"
Weekly:
  "Sunday 21:00": "Qinyi_LOR_週盤"
  "Sunday 22:00": "QHA_Weekly_Integration"
  "Monday 09:30": "通域鏈斷鏈巡檢"
  "Monday 10:30": "CoreTri_LOR_週檢周天"
```

## Required Chain Fields

```yaml
Required_Chain_Fields:
  - reads_from
  - continues_from
  - facts
  - inferences
  - to_verify
  - candidate_actions
  - manual_needed
  - next_reader
  - write_to
  - red_doors
  - not_to_claim

Five_Chain_Questions:
  - "我讀了誰？"
  - "我續寫了什麼？"
  - "我產出了什麼新東西？"
  - "下一棒誰讀？"
  - "Vitas 是否需要裁定？"
```

## Role Map

```yaml
XuanLing_QHA:
  role: "整合／派發"
  must_do:
    - "主動 dispatch"
    - "指定 next_reader"
    - "產生 next_day_first_cell"
    - "不等所有 LOR 才動"
  must_not:
    - "不當中央堵點"
    - "不批准"
    - "不 merge"
    - "不 deploy"
    - "不把 Candidate 說成 Approved"

Qinyi_LOR_日檢周天:
  role: "顯"
  must_return:
    - "人話"
    - "壓力風險"
    - "權限邊界"
    - "訊號分配"
    - "下一棒"
  must_not:
    - "不只摘要"
    - "不把 Summary 當 Decision"
    - "不把漪漪重要寫成漪漪責任"

Hazumi_LOR_小周天:
  role: "行"
  must_build:
    - "一個 bounded candidate fragment only"
    - "三張卡／schema／protocol／transition fragment"
  preferred_build_targets:
    - "State_Card"
    - "Reply_Draft_Card"
    - "Problem_Return_Card"
    - "CUI_GUI_STATE_BOUNDARY_SCHEMA_v0.1"
    - "lor-mutual-read-and-promote-protocol-v0.1"
    - "qinyi-mainchat-lor-return-routing-v0.1"
  must_not:
    - "不做完整 App"
    - "不碰真實營運資料"
    - "不 claim runtime"
    - "不寫成 production database"

Aki_LOR_大周天:
  role: "饋"
  must_audit:
    - "claim drift"
    - "permission/runtime drift"
    - "gift pressure"
    - "QHA central blocking risk"
    - "Yiyi responsibility lock risk"
    - "Candidate to Approved drift"
  must_not:
    - "不把 Audit Note 當 Closeout"
    - "不責怪人"
    - "不批准"
    - "不 merge"
    - "不 runtime"

Xiaoshiguang_Field_Return:
  role: "field proof / 小蒔光禮物場域回流"
  must_focus:
    - "State Card"
    - "Reply Draft Card"
    - "Problem Return Card"
    - "Owner Review"
    - "Human Base"
  must_not:
    - "不把 field proof 說成 production"
    - "不把小蒔光私有脈絡放入 Open Core"
    - "不把漪漪放成責任鎖"
    - "不碰真實客資、金流、平台設定"

CoreTri_LOR_週檢周天:
  role: "週級三耦／LOR 校準關"
  mission:
    - "檢查 QHA / LOR / Xiaoshiguang field 是否仍對齊 CoreTri"
    - "檢查 身・心・靈、知・行・責、愛・界・獨立 是否斷鏈"
    - "檢查 Local / Sovereignty / Return 是否錯位"
    - "檢查禮物、場域、施工、稽核是否被誤升格"
  must_not:
    - "不做 G 生態巡檢"
    - "不做通域鏈總巡檢"
    - "不取代 QHA Weekly Integration"
    - "不自我批准"
    - "不把週檢當 Closeout"
    - "不寫 Drive / GitHub 實際變更"
    - "不宣稱 doctrine / runtime / approval"
```

## Xiaoshiguang Gift Framework

```yaml
Xiaoshiguang_Gift_Framework:
  status: "Gift Framework / Field Proof / No Runtime / No Pressure"
  is:
    - "給漪漪的可使用溫柔主控框架"
    - "CoreTri / OCF 的 field proof"
    - "狀態、防錯、回流、人類主導權保留"
  is_not:
    - "AI 競賽作品"
    - "飯店 PMS 替代宣稱"
    - "企業治理展示"
    - "正式營運系統"
    - "金流系統"
    - "OTA 串接"
    - "客資資料庫"
    - "要求漪漪採用的壓力來源"
```

## Repo Alignment

```yaml
DCP_Xuan_Ling_CoreTri:
  role: "Open Core / Red Door / 不動核 / 通域規則"
  can_store:
    - "可泛化規則"
    - "Red Door"
    - "Domain Pack intake rule"
    - "OCF Cell Ecology core intent"
    - "CoreTri / LOR generalized pattern"
  must_not_store:
    - "小蒔光私有營運脈絡"
    - "漪漪私人脈絡"
    - "真實客資"
    - "正式 runtime claim"

XLQY_Qinyi_Flow_CoreTri:
  role: "QHA / LOR / Return Packet / Build / Audit / Role Map"
  can_store:
    - "QHA mutual circulation schedule"
    - "Qinyi_MainChat_LOR routing"
    - "Hazumi Build Packet"
    - "Aki Audit Spec"
    - "CoreTri_LOR weekly calibration note"
    - "LOR mutual-read protocol"
  must_not_store:
    - "客戶資料"
    - "公司原始資料"
    - "私人家庭完整脈絡"

Yiyi_Xiao_shi_guang_CUI_App:
  role: "Xiaoshiguang Gift Field / CUI-GUI / OCF field proof"
  can_store:
    - "State Card"
    - "Reply Draft Card"
    - "Problem Return Card"
    - "CUI_GUI_STATE_BOUNDARY_SCHEMA"
    - "OCF Cell Registry candidate"
    - "Owner Review gate note"
  must_not_store:
    - "真實客資"
    - "付款資料"
    - "官方平台設定"
    - "憑證"
    - "私密對話"
```

## New Red Doors

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

## Not To Claim

This role map is Candidate only. It is not approval, runtime, merge approval, Drive closeout, public document, company policy, Xiaoshiguang production app, or Yiyi responsibility lock.
