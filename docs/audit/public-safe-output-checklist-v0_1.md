# Public-Safe Output Checklist v0.1

Status: Candidate / Aki Audit Checklist / No Runtime / No Public Release Approval
Use As: public-safe review checklist before any output module, README, example, or release candidate leaves the internal carrier network
Do Not Use As: public approval, legal clearance, company approval, merge approval, or publication authorization

## Core

Public-safe means a draft appears safe for outward review. It does not mean public-approved. Aki_LOR should audit output candidates before Vitas decides whether to publish or release.

## Checklist

```yaml
Public_Safe_Check:
  contains_private_person: false
  contains_relationship_context: false
  contains_company_raw_data: false
  contains_customer_data: false
  contains_secrets_or_tokens: false
  contains_unapproved_brand_claim: false
  claims_runtime: false
  claims_approved_doctrine: false
  claims_product_ready: false
  claims_professional_approval: false
  includes_red_doors: true
  includes_not_to_claim: true
  includes_return_path: true
```

## Output Classes

```yaml
Output_Class:
  Public_Safe_Draft:
    rule: "may be reviewed, not released"
  Public_Approved:
    rule: "requires Vitas decision"
  Internal_Only:
    rule: "must not leave internal carrier"
  Red_Gate:
    rule: "hold until resolved"
```

## Red Doors

- Public-safe != Public-approved.
- Example != Production Use.
- README Draft != Release.
- Output Module Candidate != Downloadable Package.
- Aki Audit != Vitas Approval.

## Final Rule

Aki can clear a candidate for review, but only Vitas can approve external publication or release.