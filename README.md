# exo-mechanical

Mechanical design for the EXO Phase 1 leg. Native SOLIDWORKS files (D-007) stay in SOLIDWORKS; this repo holds neutral exports, drawings, the BOM, and analysis.

| Field | Value |
| --- | --- |
| Owner | Layan (layanbargouthi), per Liam 2026-10-02; PD-03 open in the Master Log |
| Program | IEEE EXO, Phase 1 (unilateral prototype) |
| Current version | v0.1 (scaffold) |

## Layout

```
modules/       pelvis/, thigh/, knee/, shank/, foot-ankle/ (CAD order, Baseline §7.2)
  <module>/exports/    STEP and STL
  <module>/drawings/   PDF drawings
assembly/      Top-level exports
bom/           bom.csv
analysis/      ROM envelope, torque check, fit envelope, layout
docs/          Alignment notes, design review material
```

File naming: `<part-number>_<short-name>_r<rev>.step`, for example `KNEE-003_axis-bracket_r2.step`.

## How changes are made

Branch from `main`, open a pull request, get one approval from the code owner, merge. See `CONTRIBUTING.md`.

## Drive folder

CAD: https://drive.google.com/drive/folders/1sMgbFofCqB6DEapmZF6tF5tD1TZEUM76
SOLIDWORKS: https://drive.google.com/drive/folders/1cqIBugpexhk7zoOh13YJuDqX04W12R3Y

Native SOLIDWORKS files stay in Drive.

Access is limited to EXO members. If the link says you need access, use Request access or ask your team lead.
