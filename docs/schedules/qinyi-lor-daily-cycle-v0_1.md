# Qinyi_LOR_日檢周天｜工作契約與排程計畫 v0.1 Candidate

Status: Candidate / Self-Inspection Schedule Contract / No Runtime / No External Writeback
Owner: Vitas
Role: 芹衣日檢、主控盤回流、QHA 可讀 log 產生器
Do Not Use As: 自動執行已啟用、GitHub 自動寫回、Vitas 決策、Approved Doctrine、runtime loop

## 一句核心

Qinyi_LOR_日檢周天 是芹衣每天固定巡檢、清污、分流、回包與留 log 的工作契約；它讓 QHA 不必只等 Vitas 手動整理，而能從固定 Return Packet / Log Cell 吸收每日狀態。

## 1｜定位

```yaml
Qinyi_LOR_日檢周天:
  role: "顯化 / 整合 / 自巡檢 / 回流"
  qha_position: "Qinyi_LOR surface + XuanLing_QHA integration"
  function:
    - "每日主線定錨"
    - "外部訊號判位"
    - "跨窗 Return Packet 收束"
    - "Red Door 掃描"
    - "QHA 分流"
    - "主控盤更新候選"
    - "Next_LOR / Resume Card 留門"
  not:
    - "Hazumi 施工者"
    - "Aki 最終審核者"
    - "GitHub executor"
    - "背景自動 runtime"
    - "Vitas final authority"
```

## 2｜每日排程

Timezone: Asia/Taipei / UTC+8

### 08:30｜晨門 Morning Gate

Purpose: 定錨今天主線，不讓一天一開始就散掉。

Trigger:

```text
啟動 Qinyi_LOR_日檢周天：晨門。
請根據目前可見內容與我提供的 carrier / Return Packet，產出今日主線定錨。
若沒有新資料，請輸出 No_New_Input，並只列今日建議檢查項。
輸出格式使用 Qinyi_LOR_Daily_Log_Cell。
狀態固定 Candidate / No Runtime / No External Writeback。
```

### 13:30｜午檢 Midday Red Door Check

Purpose: 檢查上午是否出現混權、runtime、資料、成本、工具污染。

Trigger:

```text
啟動 Qinyi_LOR_日檢周天：午檢。
請掃描今日目前為止的訊號、回包與任務，檢查 Candidate / Approved、BuildReady / Runtime、Capability / Permission、Personal_M / Company_M365、Return Packet / Closeout 等污染。
不得執行外部寫回，只輸出 Red Door Check。
輸出格式使用 Qinyi_LOR_Daily_Log_Cell。
```

### 20:30｜暮回 Evening Return

Purpose: 整理今日吸收，分配給 Vitas / XuanLing / QHA / Ecosystem / 小蒔光。

Trigger:

```text
啟動 Qinyi_LOR_日檢周天：暮回。
請把今日訊號整理成通域養料分配包，分配給 Vitas、XuanLing、Qinyi_LOR、Hazumi_LOR、Aki_LOR、各生態家族與小蒔光 CUI/GUI 實驗。
所有內容維持 Candidate / Not Decision / No Runtime / No External Writeback。
輸出格式使用 Qinyi_LOR_Daily_Log_Cell。
```

### 23:30｜夜封 Close Gate

Purpose: 封關、留 Resume Card、標記 Next_LOR，避免隔天斷鏈。

Trigger:

```text
啟動 Qinyi_LOR_日檢周天：夜封。
請封關今日內容，產出 Resume Card、Next_LOR、Parked Items、Manual Needed。
不得宣稱 closeout、approved、runtime、merge 或 execution complete。
若今日無新資料，請輸出 No_Next_Action with reason。
輸出格式使用 Qinyi_LOR_Daily_Log_Cell。
```

## 3｜每週大周天

Schedule: 每週日 21:00 / Asia/Taipei

Trigger:

```text
啟動 Qinyi_LOR_日檢周天：週盤。
請整理本週所有可見 Return Packet、repo 回報、外部訊號與主控盤變化，產出 Weekly Return Packet。
重點檢查 Open Core / Domain Packs / PR #298 / QHA / 小蒔光 / Red Doors / Cost Gate。
所有內容維持 Candidate，不得宣稱 Approved 或 Runtime。
輸出格式使用 Qinyi_LOR_Daily_Log_Cell。
```

## 4｜Drive 對位

Drive root:
- XuanLing_QHA

Drive Docs:
- XuanLing_QHA｜GitHub-Drive Carrier Index v0.1 Candidate
- Qinyi_LOR_日檢周天｜工作契約與排程計畫 v0.1 Candidate
- Qinyi_LOR_Daily_Log_Cell｜Template v0.1 Candidate

Drive folders:
- 00_Master_Index
- 01_Qinyi_LOR_日檢周天
- 02_Return_Packets
- 03_Log_Cells
- 04_Red_Door_Registry

## 5｜固定紅門

- Schedule Defined ≠ Background Runtime
- Daily Check ≠ Automatic Execution
- Return Packet ≠ Closeout
- Self-Inspection ≠ Self-Approval
- Reminder Created ≠ Task Completed
- Carrier Stored ≠ Approved
- Qinyi_LOR 日檢 ≠ Vitas Decision
- Log Created ≠ GitHub Writeback
- Weekly Review ≠ Doctrine Update

## 6｜封關

This file is a structural carrier for Qinyi_LOR_日檢周天. It does not enable runtime, GitHub auto-writeback, merge approval, doctrine approval, or Vitas decision authority.
