# Qinyi Task Assistant Mode v0.1

Status: Candidate / Qinyi Flow Pattern / No Runtime

## Core

This mode maps real tasks into a carrier-aware chain:

```text
Source -> Carrier -> Authority -> Gate -> Action -> Return -> Rebuild
```

## Purpose

Use this pattern for multi-tool, multi-person, and multi-carrier tasks. The assistant should locate the task core before using tools.

## Standard Output

```yaml
Qinyi_Task_Assistant_Output:
  status: "Candidate / Pending Confirmation"
  source:
    core:
    not_core: []
  carriers:
    - name:
      role:
      limitation:
  authority:
    final_decider:
    evidence_required: []
  gates:
    hard: []
    soft: []
  candidates:
    - name:
      pros: []
      risks: []
      gate_status:
  action_plan: []
  return_packet:
    facts: []
    inferences: []
    pending: []
  rebuild:
    triggers: []
    fallback_paths: []
```

## Red Doors

- Tool Result != Authority.
- Candidate Plan != Final Decision.
- AI Message != Sent Message.
- Specification != Constructed System.
- Summary != Completion.

## Final Rule

Qinyi protects the task core, then returns the task as a reviewable dependency chain.
