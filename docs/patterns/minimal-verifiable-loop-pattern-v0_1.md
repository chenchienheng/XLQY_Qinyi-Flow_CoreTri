# Minimal Verifiable Loop Pattern v0.1

Status: Candidate / Work Pattern / No Runtime / No External Writeback
Use As: QHA/LOR pattern for turning complex architecture into the smallest verifiable work loop
Do Not Use As: company policy, runtime spec, build approval, or closeout

## Core

When an architecture is too large to explain, QHA should not expand the explanation. It should find the smallest loop that can be built, evidenced, checked, and improved.

## Pattern

```yaml
Minimal_Verifiable_Loop:
  1_Build_Card:
    purpose: "define one bounded action"
  2_Evidence_Record:
    purpose: "record what was actually created or tested"
  3_Return_Check:
    purpose: "verify whether the loop closed"
  4_Feedback_Loop:
    purpose: "turn issues into next iteration"
```

## When To Use

```yaml
Use_When:
  - "architecture is too complex to explain"
  - "stakeholders cannot understand full system"
  - "concept drift is increasing"
  - "more documents no longer improve execution"
  - "QHA needs proof instead of more theory"
```

## LOR Roles

```yaml
Qinyi_LOR:
  role: "make the loop human-readable"
Hazumi_LOR:
  role: "build only the bounded card after approval"
Aki_LOR:
  role: "audit evidence and return check"
XuanLing_QHA:
  role: "route, integrate, and prevent blueprint expansion"
```

## Red Doors

- Explanation != Landing.
- Build Card != Build Completed.
- Evidence Record != Approval.
- Return Check != Closeout if gaps remain.
- Small Loop != Small Vision.

## Final Rule

For complex systems, land through the smallest verifiable loop. Do not ask people to understand the whole architecture before they can see one useful cycle.