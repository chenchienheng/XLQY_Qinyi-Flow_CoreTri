# XLQY Qinyi-Flow CoreTri

Status: Candidate / QHA-LOR Workface Carrier / Not Approved Doctrine / No Runtime / No Public Release Approval

## One-line Description

Qinyi Flow and QHA/LOR return layer for role-separated handoffs, log cells, build candidates, and audit feedback.

## Core

This repository organizes the XuanLing workfaces: Qinyi for human-readable framing, Hazumi for bounded build packets, Aki for return audit and red-door review, and XuanLing_QHA for dispatch and integration.

It stores role maps, dispatch templates, return packet templates, audit checklists, build packets, and mutual-circulation protocols. It is not a runtime agent, not a public product, and not the root governance source.

## Role

```yaml
Repo_Role:
  name: "XLQY_Qinyi-Flow_CoreTri"
  layer: "Flow / QHA-LOR / Return / Workface"
  use_as:
    - "QHA / LOR role maps"
    - "Qinyi work contracts"
    - "dispatch templates"
    - "Return Packet patterns"
    - "Hazumi bounded build packets"
    - "Aki audit specs"
    - "Public-safe output checklist"
    - "mutual read and circulation protocols"
  do_not_use_as:
    - "Open Core invariant source"
    - "runtime"
    - "company system"
    - "private field data"
    - "customer data carrier"
    - "public-approved doctrine"
    - "public output repo"
```

## Working Chain

```text
Source -> Carrier -> Authority -> Gate -> Action -> Return -> Rebuild
```

## QHA / LOR Workfaces

```yaml
Workfaces:
  XuanLing_QHA:
    role: "Signal Intake Gate / Carrier Router / Return Integrator"
  Qinyi_LOR:
    role: "human-readable framing / pressure and authority boundary"
  Hazumi_LOR:
    role: "bounded build packet / schema / repo skeleton candidate"
  Aki_LOR:
    role: "red-door audit / public-safe check / drift review"
```

## Current Active Reading Layer

Start with:

```yaml
QHA_Read_Order:
  1: "docs/alignment/xlqy-current-active-index-v0_1.md"
  2: "docs/dispatch/qha-daily-dispatch-template-v0_1.md"
  3: "docs/returns/minimal-hub-log-card-v0_1.md"
  4: "docs/returns/missing-return-hook-request-template-v0_1.md"
  5: "docs/audit/public-safe-output-checklist-v0_1.md"
```

## Red Doors

- Qinyi Output != Final Authority.
- Flow Template != Runtime.
- Role Map != Final Authority.
- Build Packet != Runtime.
- Audit Note != Closeout.
- Dispatch != Approval.
- Public-safe != Public-approved.
- Tool Result != Authority.
- Candidate Plan != Final Decision.

## Final Rule

XLQY organizes workfaces and returns. It protects the task core from being pulled away by tools, emotion, fragmented information, or human error, then returns each task as a learnable and rebuildable dependency chain.