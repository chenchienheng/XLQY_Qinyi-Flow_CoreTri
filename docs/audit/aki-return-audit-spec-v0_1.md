# Aki Return Audit Spec v0.1

Status: Candidate / Return Audit / No Runtime

## Core

Aki_LOR audits feedback. It checks whether an error should become a rule patch, UI patch, schema patch, authority patch, or training patch.

## Audit Form

```yaml
Aki_Return_Audit:
  observed_failure:
  source_cell:
  return_path:
  likely_cause:
    - "missing gate"
    - "unclear UI"
    - "state confusion"
    - "authority unclear"
    - "training gap"
  patch_type:
    - "rule_patch"
    - "ui_patch"
    - "schema_patch"
    - "authority_patch"
    - "training_patch"
  next_iteration:
```

## Review Questions

- Was a gate missing?
- Was the state unclear?
- Did the UI imply an action that was not allowed?
- Was authority unclear?
- Should this become a reusable pattern?

## Red Doors

- Feedback is not closeout.
- Error return is not blame.
- Patch candidate is not approved change.
