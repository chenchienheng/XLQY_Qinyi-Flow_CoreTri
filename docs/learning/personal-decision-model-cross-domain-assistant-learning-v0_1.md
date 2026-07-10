# Personal Decision Model × Cross-Domain Assistant Learning v0.1

Status: Candidate / Internal Learning / No Runtime / No External Writeback / Not Approved Doctrine
Source Case: Apple Music driving and family ambient playlist reconstruction
Primary Reader: XuanLing_QHA
Next Readers: Qinyi_LOR, Aki_LOR, Hazumi_LOR, CoreTri_LOR

## Core

A dedicated assistant should not only remember which items a user likes. It should learn the criteria by which the user accepts, rejects, reclassifies, or retains an item under different contexts.

This case supports a Context-Aware Personal Decision Model.

## Main Learning

```yaml
Context_Aware_Personal_Decision_Model:
  learns:
    - "why an item was rejected"
    - "why the same item is acceptable in one context but not another"
    - "how popularity, quality, ethics, co-listener comfort, and usability interact"
    - "how criteria update through user feedback"
  does_not_assume:
    - "one rejection means global dislike"
    - "platform availability means suitability"
    - "classification completeness means usable delivery"
```

## Key Failure Modes

```yaml
Failure_Modes:
  classification_without_function:
    red_door: "Classification Correct != Usage Experience Correct"
  safety_without_life:
    red_door: "Risk Reduction != Removal of Vitality"
  tool_match_inflation:
    red_door: "Tool Match != Semantic Match != User-Approved Match"
  batch_overbuild:
    red_door: "Batch Completion != Usable Delivery"
```

## Preference Layers

```yaml
Preference_Model_Layers:
  Stable_Identity_Preferences:
    examples:
      - "not vulgar"
      - "not cheap-looking"
      - "not excessively noisy"
      - "contemporary but not trend-following blindly"

  Context_Preferences:
    examples:
      - "driving alone"
      - "family co-listening"
      - "home ambient relief"
      - "night driving"
      - "formal work"

  Negative_Preference_Ledger:
    rule: "store rejection reason, scope, and allowed contexts"

  Positive_Retention_Logic:
    rule: "extract why an item was retained, not just find similar items"

  Confidence_and_Evidence:
    rule: "mark confidence, evidence, scope, and exclusions"

  Update_and_Return:
    chain: "Source -> Feedback -> Reason Extraction -> Scope Judgment -> Preference Patch -> Candidate Rebuild -> Tool Verification -> User Trial -> Return -> Active Model Update"
```

## Cross-Domain Application

```yaml
Applications:
  music: "playlist construction and version selection"
  procurement: "quality / maintenance / gift / formal-use criteria"
  documents: "front-end simplicity vs back-end evidence richness"
  travel: "quality, fatigue, family context, flexibility"
  interpersonal: "relationship, power distance, emotional capacity, ethics"
  schedules: "avoid notification and version explosion"
```

## Shared Red Doors

- External Popularity Signal != Personal Decision.
- Front-end Simplicity != Back-end Simplicity.
- Artifact Generated != Artifact Delivered != Artifact Adopted.
- User Trial != Failure.
- Single Feedback != Permanent Identity Rule.
- Tool Retrieval != Correct Version.
- Correct Version != Suitable Context.

## Final Rule

QHA should learn reasons, contexts, confidence, and return signals. A personal decision model must remain scoped, revisable, evidence-based, and user-authorized.