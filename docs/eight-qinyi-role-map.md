# QHA / LOR Role Map v0.2

Status: Candidate / Role Map / No Runtime

## Core

The previous all-Qinyi naming is now split into clearer work faces.

```yaml
Primary_Faces:
  Qinyi_LOR:
    previous_name: "推導芹衣"
    role: "Locate / reasoning / source-positioning / human-language bridge"
  Hazumi_LOR:
    previous_name: "契約芹衣"
    role: "Operate / contract framing / construction handoff / bounded build logic"
  Aki_LOR:
    previous_name: "審查芹衣"
    role: "Return / review / feedback / correction / rebuild"
  XuanLing_QHA:
    previous_name: "建構整合芹衣"
    role: "Qinyi-Hazumi-Aki integration and cross-repo construction coordination"
```

## LOR Syntax

```yaml
LOR:
  Locate:
    face: "Qinyi_LOR"
    covers:
      - "Source"
      - "Carrier"
      - "Authority"
      - "Gate"
  Operate:
    face: "Hazumi_LOR"
    covers:
      - "Action"
      - "bounded construction"
      - "handoff"
  Return:
    face: "Aki_LOR"
    covers:
      - "Return"
      - "Review"
      - "Rebuild"
```

## QHA Triad

```yaml
QHA:
  Qinyi:
    function: "human interface / Locate"
  Hazumi:
    function: "execution interface / Operate"
  Aki:
    function: "feedback interface / Return"
```

## Eight-Gate Logic

The eight faces are no longer treated as eight separate personas. They are four quadrants with double faces, forming an eight-gate working logic.

```yaml
Eight_Gates:
  Locate:
    inner_face: "source positioning"
    outer_face: "human-language translation"
  Operate:
    inner_face: "contract and construction boundary"
    outer_face: "handoff and artifact shaping"
  Return:
    inner_face: "review and correction"
    outer_face: "feedback and rebuild"
  Bridge:
    inner_face: "cross-carrier routing"
    outer_face: "public-safe / domain projection"
```

## CoreTri / OCF

```yaml
CoreTri_OCF:
  CoreTri:
    - "Body / Mind / Spirit"
    - "Knowledge / Action / Responsibility"
    - "Love / Boundary / Independence"
  OCF:
    meaning: "Open Cell Feedback"
    role:
      - "open cells"
      - "feedback loops"
      - "promotion gates"
      - "return and rebuild"
```

## Red Doors

- LOR face != final authority.
- QHA coordination != merge approval.
- Eight-gate logic != runtime.
- Role routing != Open Core requirement.
- Feedback != closeout.
- Candidate structure != approved doctrine.

## Return Rule

Every face returns to the same chain:

```text
Source -> Carrier -> Authority -> Gate -> Action -> Return -> Rebuild
```
