# Context-Aware Personal Decision Model v0.1

Status: Candidate / Personal Decision Model / No Runtime / No External Writeback
Use As: assistant-side preference and judgment structure for scoped, reversible personalization
Do Not Use As: permanent personality profile, psychological diagnosis, autonomous decision authority, or cross-context global rule

## Core

Personalization should model criteria, context, confidence, evidence, and update path—not merely favorite items.

## Minimal Structure

```yaml
Personal_Decision_Model:
  user_id:
  domain:
  context:
  stable_criteria: []
  context_criteria: []
  external_signals: []
  rejection_ledger:
    - item:
      reason: []
      scope: []
      allowed_elsewhere: []
      global_ban: false
  retention_logic:
    - criterion:
      evidence: []
  version_gate:
    reject_variants: []
  confidence_records:
    - criterion:
      confidence: "low / medium / high"
      evidence: []
      applies_to: []
      does_not_apply_to: []
  authority:
    candidate_by: "QHA"
    final_by: "Vitas"
  return_signals:
    - "used"
    - "skipped"
    - "deleted"
    - "reclassified"
    - "retained"
```

## Decision Flow

```text
External Signal
-> Candidate Pool
-> Context Gate
-> Value / Clean / Risk Gate
-> Version / Object Verification
-> User Trial
-> Retain / Reject / Reclassify
-> Preference Patch
-> Active Model Update
```

## Confidence States

```yaml
Preference_Status:
  Confirmed: "explicitly stated or repeatedly evidenced"
  High_Confidence_Inference: "strong pattern with bounded scope"
  Candidate_Criterion: "plausible but not yet tested"
  To_Verify: "insufficient evidence"
```

## Front-End / Back-End Rule

```text
Back-end Governance Richness != Front-end Cognitive Load
```

The internal model may preserve source, reason, scope, version, and confidence. The user-facing surface should show only the shortest useful decision label for the context.

## Red Doors

- One rejection != global dislike.
- Context preference != stable identity.
- Popularity != suitability.
- Tool retrieval != correct object.
- Correct object != suitable choice.
- Suitable choice != user approval.
- Assistant inference != user identity.

## Final Rule

The model must remain scoped, evidence-based, confidence-rated, reversible, and updated through user return rather than silently fixed.