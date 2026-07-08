# Tri-Repo Flow Return Protocol v0.1

Status: Candidate / Flow Return Protocol / No Runtime / No External Writeback
Use As: XLQY protocol for mediating Core -> Flow -> Field -> Return cycles
Do Not Use As: approval, runtime automation, merge instruction, or final authority

## Core

XLQY is not a storage repo. It is the workface membrane between Core governance and Field proof. It must translate Core rules into QHA/LOR tasks and return field results as bounded return packets.

## Flow Direction

```yaml
Flow_Cycle:
  Core_to_Flow:
    input:
      - "Signal Intake Gate"
      - "Production Router"
      - "Small Build Loop Gate"
      - "Authority Ring Map"
    output:
      - "QHA Dispatch"
      - "Qinyi human-readable layer"
      - "Hazumi build packet candidate"
      - "Aki audit request"

  Flow_to_Field:
    input:
      - "bounded build packet"
      - "field card spec"
      - "red doors"
    output:
      - "field proof request"

  Field_to_Flow:
    input:
      - "state card result"
      - "reply draft issue"
      - "problem return"
    output:
      - "return packet"
      - "missing hook request"
      - "audit request"

  Flow_to_Core:
    input:
      - "generalized pattern"
      - "red door patch"
      - "router patch"
    output:
      - "DCP candidate update request"
```

## LOR Roles

```yaml
LOR_Roles:
  Qinyi_LOR: "human-readable translation and pressure boundary"
  Hazumi_LOR: "bounded build packet only after gate"
  Aki_LOR: "red-door and public-safe audit"
  XuanLing_QHA: "dispatch, index, return integration"
```

## Red Doors

- Flow Repo != Passive Storage.
- Dispatch != Approval.
- Build Packet != Runtime.
- Audit Note != Closeout.
- Field Return != Root Doctrine.

## Final Rule

XLQY should maintain the living membrane between Core rules and Field proof. It should never become the root doctrine or the field data store.