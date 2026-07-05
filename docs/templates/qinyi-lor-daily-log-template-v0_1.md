# Qinyi_LOR_Daily_Log_Cell｜Template v0.1 Candidate

Status: Candidate / Log Template / No Runtime / No External Writeback
Owner: Vitas
Role: Qinyi_LOR 日檢周天輸出格式、QHA 可讀 log cell、Drive/GitHub 對鏈模板

## 一句核心

Qinyi_LOR_Daily_Log_Cell 是每次晨門、午檢、暮回、夜封與週盤的共同輸出格式；它讓 XuanLing_QHA 可以固定吸收每日狀態，但不代表自動執行、批准或外部寫回。

## Template

```yaml
Qinyi_LOR_Daily_Log_Cell:
  date:
  timezone: "Asia/Taipei / UTC+8"
  phase: "晨門 / 午檢 / 暮回 / 夜封 / 週盤"
  trigger_source:
  input_carriers:
    github:
    drive:
    chat:
    manual_input:
  facts:
  inferences:
  to_verify:
  candidate_signals:
  red_doors:
  candidate_actions:
  manual_needed:
  return_targets:
  parked_items:
  qha_distribution:
    qinyi_lor:
    hazumi_lor:
    aki_lor:
    xuanling_qha:
  next_lor:
  resume_card:
  not_to_claim:
    - "Not Approved"
    - "No Runtime"
    - "No External Writeback"
    - "Return Packet ≠ Closeout"
    - "Log Created ≠ GitHub Writeback"
```

## Phase Rules

### 晨門 Morning Gate

- 定錨今日主線。
- 若無新資料，輸出 `No_New_Input`。
- 不直接產生 execution claim。

### 午檢 Midday Red Door Check

- 掃描 Candidate / Approved、BuildReady / Runtime、Capability / Permission、Personal_M / Company_M365、Return Packet / Closeout 污染。
- 僅輸出 Red Door Check。

### 暮回 Evening Return

- 整理今日訊號。
- 分配給 Vitas / XuanLing / Qinyi_LOR / Hazumi_LOR / Aki_LOR / Ecosystem Families / Xiaoshiguang。
- 保持 Candidate / Not Decision。

### 夜封 Close Gate

- 產出 Resume Card、Next_LOR、Parked Items、Manual Needed。
- 不宣稱 closeout、approved、runtime、merge 或 execution complete。

### 週盤 Weekly Major Cycle

- 檢查 Open Core / Domain Packs / PR #298 / QHA / 小蒔光 / Red Doors / Cost Gate。
- 產出 Weekly Return Packet Candidate。

## Storage Rule

Drive location:

```text
XuanLing_QHA/03_Log_Cells/YYYY-MM-DD/
```

GitHub canonical template:

```text
chenchienheng/XLQY_Qinyi-Flow_CoreTri
docs/templates/qinyi-lor-daily-log-template-v0_1.md
```

Boundary:

- Drive log is human-readable carrier.
- GitHub template is structural carrier.
- Neither is runtime, merge approval, or Vitas decision.
