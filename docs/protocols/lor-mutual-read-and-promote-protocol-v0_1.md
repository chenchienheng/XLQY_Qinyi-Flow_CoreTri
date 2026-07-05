# LOR Mutual Read and Promote Protocol v0.1

Status: Candidate / Mutual Read Protocol / No Runtime

## Core

LOR windows should not wait in a one-way chain. Each LOR can read bounded returns from the others and promote useful signals back to QHA.

## Mutual Read Map

```yaml
Qinyi_LOR:
  reads:
    - "MainChat_LOR returns"
    - "Aki audit notes"
    - "QHA dispatch"
  returns:
    - "human context"
    - "pressure risk"
    - "authority boundary"

Hazumi_LOR:
  reads:
    - "QHA dispatch"
    - "Qinyi human-context return"
    - "field context"
  returns:
    - "build packet"
    - "blocked units"
    - "staging plan"

Aki_LOR:
  reads:
    - "QHA schedule"
    - "Hazumi build candidates"
    - "Qinyi pressure-risk return"
  returns:
    - "audit note"
    - "rule patch"
    - "authority patch"
```

## Promote Rule

A return can be promoted only when it has source, carrier, authority boundary, red-door scan, and return path.

## Red Doors

- LOR != Passive Subordinate.
- QHA != Central Blocking Node.
- Mutual Read != Merge Approval.
- Candidate Promote != Approved Promote.
- Feedback != Closeout.

## Final Rule

LOR windows are circulation faces. They should read, return, and promote bounded signals without becoming autonomous authority.
