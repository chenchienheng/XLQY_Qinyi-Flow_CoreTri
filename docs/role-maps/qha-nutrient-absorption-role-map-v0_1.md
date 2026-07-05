# QHA Nutrient Absorption Role Map v0.1

Status: Candidate / Role Map / No Runtime
Source: Daily Signal Nutrient Distribution Pack 2026-07-05

## Core

Daily signals should be routed by role. QHA does not absorb everything in the same way.

## Role Absorption

```yaml
QHA_Nutrient_Absorption:
  Qinyi_LOR:
    absorbs:
      - "Facts / Inferences / To Verify"
      - "human-language translation"
      - "pressure and authority visibility"
    returns:
      - "candidate signal summary"
      - "manual needed"
      - "return packet"

  Hazumi_LOR:
    absorbs:
      - "buildable document candidates"
      - "schemas"
      - "review matrices"
      - "CUI / GUI specs"
    returns:
      - "build packet"
      - "staging plan"
      - "blocked units"

  Aki_LOR:
    absorbs:
      - "claim inflation risk"
      - "permission drift"
      - "runtime drift"
      - "missing To Verify"
    returns:
      - "audit note"
      - "rule patch"
      - "UI / schema / authority patch"

  XuanLing_QHA:
    absorbs:
      - "generalizable pattern"
      - "field-specific boundary"
      - "repo placement"
      - "red-door update"
    returns:
      - "pattern index"
      - "domain routing"
      - "promotion gate"
```

## Red Doors

- QHA route is not final authority.
- Signal summary is not decision.
- Build packet is not runtime.
- Audit note is not closeout.
- Field signal is not Open Core by default.

## Final Rule

A signal is useful only after it reaches the correct QHA face and returns with a bounded next action.
