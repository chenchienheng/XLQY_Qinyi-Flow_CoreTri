# QHA LOR Chain Experiment Dispatch v0.1

Status: Candidate / Cross-Window Dispatch / Internal Chain Experiment / No Runtime / No GitHub Merge / No External Writeback / No Closeout
Date: 2026-07-07
Primary Receiver: QHA_Daily_Dispatch
First Gate: Signal Intake Gate
Final Authority: Vitas

## Core

This packet chains the current architecture experiment into QHA daily dispatch. It must not directly dispatch Hazumi construction. QHA should first classify signals, create active pointer row candidates, and assign next readers.

## Signal Intake Gate Result

```yaml
QHA_Gate_Result:
  decision: "Candidate_GO / Read-Only Chain Experiment"
  allowed:
    - "read"
    - "classify"
    - "dispatch"
    - "return packet"
    - "pointer row candidate"
  forbidden:
    - "direct Hazumi construction"
    - "GitHub merge"
    - "public release"
    - "runtime deployment"
    - "company data touch"
    - "formal BIM/CAD model execution"
```

## Themes to Chain

```yaml
Themes:
  Carrier_Registry_v0_2:
    next_reader: ["Qinyi_LOR", "Aki_LOR", "Ecosystem_Architecture_Experiment"]
  Production_Router_v0_1:
    next_reader: ["Qinyi_LOR", "XuanLing_QHA"]
  Output_Repo_Skeleton_v0_1:
    next_reader: ["Hazumi_LOR", "Aki_LOR"]
    condition: "Hazumi produces candidate only after Vitas allows build packet"
  BIM_CAD_Open_Host_Bridge_v0_1:
    next_reader: ["Hazumi_LOR", "Aki_LOR", "Ecosystem_Architecture_Experiment"]
  Origin_Trust_Anchor_Patch:
    next_reader: ["XuanLing_QHA", "Aki_LOR", "Qinyi_LOR"]
    condition: "internal-only, no public repo details"
  Software_Skills_Registry_v0_2:
    next_reader: ["Ecosystem_Architecture_Experiment", "Qinyi_LOR", "Aki_LOR"]
```

## Active Pointer Row Candidates

```yaml
Active_Pointer_Rows:
  - id: "CR-001"
    name: "Carrier Registry v0.2 Candidate"
    owner_window: "XuanLing_QHA"
    next_reader: "Qinyi_LOR / Aki_LOR"
    status: "Candidate"
  - id: "PR-001"
    name: "Production Router v0.1 Candidate"
    owner_window: "Qinyi_LOR"
    next_reader: "XuanLing_QHA"
    status: "Candidate"
  - id: "OM-001"
    name: "Output Repo Skeleton v0.1 Candidate"
    owner_window: "Hazumi_LOR"
    next_reader: "Aki_LOR"
    status: "Candidate"
  - id: "BIM-001"
    name: "BIM_CAD_Open_Host_Bridge v0.1 Candidate"
    owner_window: "Hazumi_LOR"
    next_reader: "Aki_LOR / Ecosystem_Architecture_Experiment"
    status: "Candidate"
  - id: "ORG-001"
    name: "Origin / Trust Anchor Patch v0.1 Candidate"
    owner_window: "XuanLing_QHA"
    next_reader: "Aki_LOR / Qinyi_LOR"
    status: "Internal Only"
  - id: "SW-001"
    name: "Software / Skills Carrier Registry v0.2 Candidate"
    owner_window: "Ecosystem_Architecture_Experiment"
    next_reader: "Qinyi_LOR / Aki_LOR"
    status: "Candidate"
```

## Required Return Fields

- facts
- inferences
- to_verify
- manual_needed
- red_doors
- next_reader
- write_to
- not_to_claim

## Red Doors

- QHA Dispatch != Approval.
- Signal Intake Gate != Decision.
- Candidate Pointer != Active Truth.
- Hazumi Candidate != Construction Approval.
- Origin Context != Public Story.
- BIM/CAD Bridge != Production Model Execution.
- Output Repo Skeleton != Public Release.

## Manual Needed

- Vitas approve output repo name.
- Vitas approve module scope.
- Vitas approve any GitHub writeback beyond candidate docs.
- Vitas approve any Hazumi construction.

## Final Rule

QHA Daily Dispatch receives this packet first. It classifies, creates pointer candidates, and assigns next readers. It does not directly authorize construction.