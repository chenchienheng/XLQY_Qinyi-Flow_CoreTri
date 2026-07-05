# QHA Mutual Circulation Schedule v0.1

Status: Candidate / Internal Circulation / No Runtime / No External Writeback
Source: Qinyi_MainChat_LOR return
Use As: circulation schedule for XuanLing_QHA and LOR windows
Do Not Use As: doctrine, runtime schedule, merge approval, or external writeback

## Core

QHA should not wait passively for all LOR windows. QHA should dispatch reading tasks, request bounded returns, and integrate logs into the shared chain.

```text
MainChat_LOR -> QHA Dispatch -> Qinyi_LOR / Aki_LOR / Hazumi_LOR -> QHA Integration -> Vitas Decision Queue
```

## Cycles

```yaml
Small_Cycle:
  name: "QHA Daily LOR Dispatch"
  purpose:
    - "read new MainChat_LOR signals"
    - "assign LOR reading tasks"
    - "request bounded returns"
  output:
    - "QHA_Daily_Dispatch_Packet"
    - "LOR_Reading_Assignment"

Medium_Cycle:
  name: "QHA 3-Day Cross-LOR Check"
  purpose:
    - "check whether LOR windows read each other"
    - "detect one-way waiting"
    - "repair missing return hooks"
  output:
    - "Cross_LOR_Circulation_Check"
    - "Blocked_Loop_Report"

Large_Cycle:
  name: "XuanLing QHA Weekly Return"
  purpose:
    - "extract generalized rules"
    - "separate fieldspace and Open Core"
    - "prepare Vitas decision queue"
  output:
    - "Weekly_QHA_Return"
    - "Candidate_Repo_Placement"
    - "Red_Door_Update"
```

## Red Doors

- QHA != Central Blocking Node.
- LOR != Passive Subordinate.
- No LOR Update != QHA Cannot Move.
- Schedule Spec != Runtime Automation.
- Candidate Dispatch != Merge Approval.

## Final Rule

QHA must keep circulation alive by dispatching, reading, integrating, and returning. It must not become a waiting bottleneck.
