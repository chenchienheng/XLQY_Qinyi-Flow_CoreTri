# XLQY Superseded / Reference Index v0.1

Status: Candidate / Superseded Reference Index / No Runtime / No External Writeback / No Deletion
Repo: chenchienheng/XLQY_Qinyi-Flow_CoreTri

## Core

This index is the first pass for classifying older or duplicate XLQY workface files. It does not delete, move, or invalidate any file.

## Classification Rows

```yaml
XLQY_Superseded_Reference:
  Reference_Pending:
    meaning: "useful lineage, not current workface reading layer"
    examples:
      - "older Qinyi/Hazumi/Aki role drafts"
      - "long return packets replaced by templates"
      - "older mutual circulation notes"

  Superseded_Pending:
    meaning: "likely replaced by active dispatch or protocol files"
    examples:
      - "pre-One-Hub multi-window schedule notes"
      - "old QHA external-third-party wording before self-addressing rule"
      - "older missing-hook descriptions before template"

  Archive_Pending:
    meaning: "historical material to keep out of current workface"
    examples:
      - "stage return packets already converted to active index"
      - "full text reports after essence extraction"

  Keep_Active:
    meaning: "listed in XLQY Current Active Index"
    pointer: "docs/alignment/xlqy-current-active-index-v0_1.md"
```

## Review Needed

QHA should later compare actual files against current-active-index and propose path-level classifications.

## Red Doors

- Superseded Pending != Superseded Confirmed.
- Reference != Current Truth.
- Archive Pending != Deletion.
- Classification != File Move.
- Role Draft != Final Authority.

## Final Rule

XLQY cleanup should protect the current QHA/LOR workface from older role drift and long-packet pollution.