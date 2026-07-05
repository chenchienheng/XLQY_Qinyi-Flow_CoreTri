# QHA Cycle Log Import Index｜2026-07-05 v0.1

Status: Candidate / Import Index / Not Approved / No Runtime / No External Writeback
Owner: Vitas
Carrier: XLQY_Qinyi-Flow_CoreTri
Source: Hazumi_LOR scheduled task carrier-map update on 2026-07-05 Asia/Taipei
Do Not Use As: Approved doctrine, runtime, GitHub merge approval, Drive write confirmation, external automation, or closeout.

## Core

Hazumi_LOR scheduled output must not remain as isolated chat text. Each Cycle Log should carry a QHA import key and a candidate carrier placement so XuanLing_QHA can classify, absorb, park, or route it.

```text
Scheduled Chat Output -> QHA Import Key -> Candidate Import Index -> Manual / Authorized Carrier Write -> QHA Daily Absorption -> Aki Audit / Vitas Decision
```

## Import Key

```yaml
QHA_Import_Key:
  format: "HAZUMI-LOR-YYYYMMDD-CYCLE-A|B"
  status: "Candidate / Not Approved / No Runtime / No External Writeback"
  source_required: true
  empty_source_behavior: "No_New_Source / Parked / Next_Cell_Requires_Vitas_Input"
```

## Candidate Carrier Placement

```yaml
Drive_Working_Inbox:
  folder: "XuanLing_QHA_Cycle_Log_Inbox"
  index_doc: "XuanLing_QHA_Hazumi_Cycle_Log_Import_Index_v0.1_Candidate"
  status: "Suggested / Not Created Here / Requires Explicit Write Permission"

GitHub_XLQY_Qinyi_Flow_CoreTri:
  primary_import_index: "docs/returns/qha-cycle-log-import-index-YYYY-MM-DD.md"
  build_packets: "docs/build-packets/"
  audits: "docs/audit/"
  status: "Candidate import carrier"

GitHub_DCP_Xuan_Ling_CoreTri:
  governance_routing: "docs/governance/qha-scheduled-carrier-routing-YYYY-MM-DD-v0_1.md"
  signals: "docs/signals/"
  github_rules: "docs/github/"
  status: "Root routing / red-door carrier"

GitHub_Yiyi_Xiao_shi_guang_CUI_App:
  experiments: "docs/experiments/"
  ocf: "docs/ocf/"
  return: "docs/return/"
  status: "Suggested only unless Xiaoshiguang field source is active"
```

## QHA Daily Absorption Read Rule

```yaml
QHA_Daily_Read_Rule:
  reads:
    - "Hazumi_LOR_Cycle_Log entries available in scheduled-chat context"
    - "QHA import key"
    - "suggested carrier placement"
  does_not_assume:
    - "Drive file exists"
    - "GitHub file was committed"
    - "repo path is approved mainline"
    - "scheduled output is closeout"
  if_missing_logs:
    output: "cycles_received: 0"
    next_cell: "Requires_Vitas_Input"
```

## Red Doors

- Scheduled Chat Output ≠ Repo File
- Suggested Carrier Placement ≠ External Writeback
- GitHub Commit ≠ Merge Approval
- Drive Doc ≠ Closeout
- QHA Daily Absorption ≠ Approved Doctrine
- Return Packet ≠ Closeout
- Tool Capability ≠ Permission
- Needs Vitas Decision ≠ Approved

## Current Task Linkage

```yaml
Minimum_Task_Set:
  Hazumi_LOR:
    cadence: "hourly task outputting two 30-minute Cycle Logs"
    required_fields:
      - cycle_id
      - timestamp
      - qha_import_key
      - source
      - carrier
      - selected_cell
      - built_candidate
      - suggested_carrier_placement
      - red_doors_checked
      - blocked_items
      - manual_needed
      - return_packet
      - next_cell
      - not_to_claim
  QHA_Daily_Big_Cycle:
    cadence: "daily after work"
    function: "absorb, classify, park, and route available Hazumi logs"
```

## Not To Claim

This file is an import index candidate. It does not prove that scheduled logs were written to Drive, merged into GitHub, approved by Vitas, or deployed as runtime.
