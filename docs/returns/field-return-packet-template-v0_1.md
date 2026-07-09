# Field Return Packet Template v0.1

Status: Candidate / Return Template / No Runtime / No External Writeback
Use As: XLQY return packet template for sanitized Field-to-Flow returns
Do Not Use As: raw field data transfer, production closeout, owner approval, or public release material

## Core

Field returns must be sanitized, bounded, and useful. The Field repo returns card evidence, problem patterns, red doors, and generalized lessons through XLQY before any pattern can be considered by DCP.

## Template

```yaml
Field_Return_Packet:
  return_id:
  source_repo: "Yiyi_Xiao-shi-guang-CUI-App"
  source_card:
  card_type: "State_Card / Reply_Draft_Card / Problem_Return_Card"
  reads_from: []
  field_evidence_summary:
  sanitized_pattern:
  red_doors_triggered: []
  private_context_removed: true
  facts: []
  inferences: []
  to_verify: []
  candidate_actions: []
  manual_needed: []
  next_reader:
  write_to:
  not_to_claim: []
```

## Minimum Requirements

- No real guest data.
- No private messages.
- No payment records.
- No platform credentials.
- No production runtime claim.
- Include next_reader and write_to.

## Red Doors

- Field Return != Raw Field Context.
- Sanitized Pattern != Root Doctrine.
- Card Evidence != Runtime Proof.
- Next Reader != Approval.
- Return Packet != Closeout.

## Final Rule

A Field Return can move through XLQY only when it is sanitized, bounded, and linked to a next reader.