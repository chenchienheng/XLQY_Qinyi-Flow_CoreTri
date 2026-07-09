# M365 Human-Controlled File Manifest Build Card v0.1

Status: Candidate / Build Card / Human-Gated / No Runtime / No External Writeback / Not Company Submission
Use As: small-loop build card for testing human-controlled file manifest classification
Do Not Use As: company IT report, production workflow, external connector spec, company data extraction, or automated scanning approval

## Core

This build card tests whether a human-controlled file manifest can support classification and review without moving original documents or granting AI direct access to company content.

## Purpose

Create a minimal manifest loop:

```text
authorized folder
-> filelist manifest
-> classification table
-> human review
-> evidence record
-> return check
```

## Input

```yaml
Input:
  authorized_folder: "human-selected only"
  manifest_file: "filelist.csv / sanitized manifest"
  allowed_metadata:
    - "file path or sanitized path"
    - "file name"
    - "extension"
    - "size"
    - "last modified time"
  forbidden:
    - "file content ingestion by default"
    - "company secrets"
    - "customer data"
    - "credentials"
    - "automatic external upload"
```

## Output Table

```yaml
Manifest_Output_Columns:
  - File_Path
  - File_Name
  - Extension
  - Project
  - Discipline
  - Document_Type
  - Possible_Use
  - Sensitivity
  - Need_Review
  - Reviewer
  - Status
```

## Steps

1. Human selects an authorized folder.
2. Human generates a manifest file.
3. AI or Copilot classifies manifest rows only.
4. Human reviews the classification.
5. Create Evidence Record.
6. Run Return Check.

## Evidence Required

- manifest file location
- sample classified rows
- reviewer name or role
- red-door notes
- confirmation that no original file content was moved or uploaded

## Red Doors

- Manifest != Original Content.
- Index Can Assist != Authorization Can Be Bypassed.
- Human-Controlled Input != External Auto-Writeback.
- Filelist Exists != File Reviewed.
- Classification != Approval.
- Evidence Missing != Completed.

## Final Rule

The manifest may move; the original content does not move by default. Human review remains the gate.