# Personal Decision Model｜Music Playlist Case v0.1

Status: Candidate / Internal Learning / No Runtime / No External Writeback / Not Approved Doctrine
Source Case: Apple Music driving and family ambient playlist reconstruction
Use As: cross-domain learning packet for QHA, Qinyi, Aki, and recommendation/personalization workfaces
Do Not Use As: permanent personality profile, automated preference enforcement, public user profile, or final recommendation doctrine

## Core

A dedicated assistant should not merely remember which items a user liked. It should learn which criteria caused the user to retain, reject, reclassify, or limit an item in a specific context.

## Main Finding

```yaml
Context_Aware_Personal_Decision_Model:
  stable_preferences:
    - "not vulgar"
    - "not cheap or low-quality"
    - "not excessively noisy"
    - "contemporary without blindly following trends"
    - "quality should not be lowered to fill a list"
  context_preferences:
    solo_driving: "more rhythm and exploration allowed"
    family_driving: "low embarrassment, low stimulation, safe to share"
    home_ambient: "no vocal or low semantic burden, low dynamic contrast"
    night_driving: "continuous, medium tempo, low fatigue"
  negative_ledger:
    rule: "record why an item was rejected, the scope, and where it may still be allowed"
  positive_retention:
    rule: "extract why an item stayed instead of copying superficially similar items"
  confidence:
    rule: "separate explicit confirmation, high-confidence inference, candidate criterion, and pending trial"
```

## Failure Modes Observed

- Classification correct does not mean experience correct.
- Clean does not mean obscure, old-fashioned, or lifeless.
- Platform retrieval does not mean semantic match or user-approved match.
- Batch completion does not mean usable delivery.
- Multiple versions without Active / Superseded / Archive create pollution.
- Front-end names must respect operating context and cognitive load.

## Key Red Doors

- Tool Match != Semantic Match.
- Semantic Match != User-Approved Match.
- External Popularity Signal != Personal Decision.
- Explicit Label Missing != Socially Safe.
- Artifact Generated != Artifact Delivered.
- Artifact Delivered != Artifact Adopted.
- One Rejection != Global Ban.
- One Positive Interaction != Permanent Preference.

## Preference Update Loop

```text
Source
-> User Feedback
-> Reason Extraction
-> Scope Judgment
-> Preference Patch
-> Candidate Rebuild
-> Tool Verification
-> User Trial
-> Return
-> Active Model Update
```

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
  retention_logic: []
  confidence_records: []
  version_gate:
    reject_variants: []
  authority:
    candidate_by: "QHA"
    final_by: "Vitas"
  return:
    - "played"
    - "skipped"
    - "deleted"
    - "reclassified"
    - "retained"
```

## Cross-Domain Generalization

The same model can support procurement, reports, travel, communication, scheduling, and lifestyle choices. The system must learn decision criteria and context boundaries, not merely repeat previous selections.

## Final Rule

Negative feedback is not failure. It is high-value ground-truth input when the reason, scope, confidence, and return path are preserved.