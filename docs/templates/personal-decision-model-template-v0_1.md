# Personal Decision Model Template v0.1

Status: Candidate / QHA-Qinyi Learning Template / No Runtime / No External Writeback
Use As: structured template for context-aware user judgment learning across music, procurement, documents, travel, communication, schedules, and life management
Do Not Use As: psychological diagnosis, immutable personality profile, automated decision authority, or global preference lock

## Core

Record why a user accepted, rejected, retained, or reclassified an item. Every preference must include context, scope, confidence, evidence, and an update path.

## Template

```yaml
Personal_Decision_Model:
  user_id:
  domain:
  context:

  stable_criteria:
    - criterion:
      confidence:
      evidence: []

  context_criteria:
    - context:
      criteria: []

  rejection_ledger:
    - item:
      rejected_from:
      reason: []
      allowed_elsewhere: []
      global_ban: false
      confidence:

  retention_ledger:
    - item:
      retained_because: []
      reusable_features: []
      confidence:

  external_signals:
    - source:
      signal_type:
      signal_value:
      does_not_decide: []

  version_gate:
    reject_versions: []
    preferred_versions: []
    verification_required: true

  authority:
    candidate_by: "QHA / assistant"
    final_by: "Vitas"

  return:
    - played_or_used
    - skipped_or_rejected
    - deleted
    - reclassified
    - retained

  update_status:
    current_state: "Candidate"
    supersedes:
    superseded_by:
    next_review:
```

## QHA Rules

1. Build criteria before generating large option sets.
2. Rejection reason has more value than rejected item alone.
3. Every preference must declare context and scope.
4. External popularity enters Candidate Pool only.
5. Tool results require semantic and version verification.
6. Front-end names must fit operational cognitive load.
7. Build one reviewable unit at a time.
8. Mark old versions Active / Superseded / Archive.
9. User trial is calibration evidence, not failure.
10. Distinguish confirmed preference, high-confidence inference, candidate criterion, and unverified assumption.

## Red Doors

- Preference != Identity.
- Local Criterion != Global Rule.
- User Trial != Failure.
- Popular != Suitable.
- Tool Result != Final Choice.
- Generated Options != Delivered Experience.

## Final Rule

A dedicated assistant should learn how the user judges—not merely what the user selected.