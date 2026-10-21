# exo-mechanical

Mechanical design for the EXO Phase 1 leg. SOLIDWORKS is the CAD platform. Native SOLIDWORKS files stay in Drive; this repo holds neutral exports, drawings, the BOM, and analysis.

| Field | Value |
| --- | --- |
| Owner | Mechanical lead |
| Program | IEEE EXO, Phase 1 (unilateral prototype) |
| Current version | v0.1 (scaffold) |

## Current work

Each package lists its sub-team, its deliverables, what shows the work is done, and the Drive folder for its files. Owner for every package: assigned by the Mechanical lead. Dates are planned targets.

### Active

**MECH-005 Hip Assembly and Battery Integration**
- Sub-team: Conquistadors. Drive folder: [Conquistadors](https://drive.google.com/drive/folders/1-N154LxBfmxJU8Cz5WTFKkoVAxI1Gutl)
- Deliverables:
  - Hip assembly: mechanical design of the hip actuator mounting system and its connection to the exoskeleton frame.
  - Battery placement: 12 Molicel P45B 21700 cells in a 2 x 6 arrangement with space reserved for the BMS candidate, carried on a belt. Enclosure insulation approach to be confirmed by the Project Leads.
  - Thermal management: heat generation and ventilation requirements.
  - Component mounting: electronics positioning.
- Shows it is done: (1) a preliminary SOLIDWORKS assembly with the AK80-9 STEP imported; (2) a battery enclosure concept with estimated dimensions, each dimension cited to a datasheet or measurement; (3) mounting and thermal considerations, with heat inputs from Electrical stated in watts as received inputs.
- Fit mockups use dummy cell models only.
- Owner: assigned by the Mechanical lead.

**MECH-006 Hip-to-Knee Mechanical Design**
- Sub-team: Hip-to-Knee Mechanical Design. Drive folder: [Hip-to-Knee Mechanical Design](https://drive.google.com/drive/folders/18588fo7UQuo68TrtYW9ZAdcWz2FaoHSn)
- Deliverables:
  - Free-body diagrams for the hip-to-knee assembly: external forces, joint loads, actuator reactions. State the user mass assumed; the target user mass and height range are to be confirmed by the Project Leads.
  - Investigation of a sagittal-plane joint mechanism: a linkage that allows hip and knee flexion and extension while maintaining alignment. Whether sideways joint motion is included is to be confirmed by the Project Leads.
  - Knee actuator housing: initial design accounting for protection, mounting, and range of motion, with the knee hard stop at 0 degrees extension.
  - Telescoping mechanism: adjustable connections for different leg lengths with structural rigidity.
  - Wiring mockup: potential wiring routes through the assembly, with clearance during joint movement.
- Shows it is done: the free-body diagram set with its assumptions; initial joint and knee enclosure CAD concepts; a telescoping adjustment concept; a preliminary wiring layout showing routes and clearance through joint motion.
- Owner: assigned by the Mechanical lead.

**MECH-007 Passive Ankle Mechanism**
- Sub-team: Kit-Kat. Drive folder: [Kit-Kat](https://drive.google.com/drive/folders/1XF-sLztf0rqBe9-xesQuOoOimf46Rgle)
- Deliverables:
  - Clutch options that engage or disengage ankle assistance during gait phases.
  - Ratchet-based designs for controlling or restricting ankle motion.
  - A comparison of the clutch and ratchet concepts on reliability, size, weight, mechanical complexity, and gait compatibility.
  - How the selected mechanism interacts with a spring-based ankle assistance system.
- Shows it is done: a selection matrix scoring both concepts on the five criteria; the selected mechanism concept with written justification; a preliminary mechanical layout in SOLIDWORKS; a description of the spring interaction.
- How the clutch is triggered is to be confirmed by the Project Leads.
- Owner: assigned by the Mechanical lead.

**MECH-001 ROM safety envelope and peak-torque table**
- Deliverable: a single cited range-of-motion safety envelope and peak-torque table, reconciling the two slide variants (ankle dorsiflexion, ankle plantarflexion, hip abduction and adduction).
- Shows it is done: one table with a source for each row.
- Owner: assigned by the Mechanical lead.

### Update expectation

The Conquistadors give an update on Tuesday, planned Oct 27. The update shows work in progress. No one is expected to be finished by then.

### Queued next

Torque check, anthropometric measurement set, one-leg layout.

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

## Where files live

Native SOLIDWORKS files, bench logs, test data, photos, and vendor PDFs live in Drive. This repo holds exports, drawings, the BOM, code, and short summaries. Exports are STEP and STL, drawings are PDF, and the BOM is CSV.

CAD: https://drive.google.com/drive/folders/1sMgbFofCqB6DEapmZF6tF5tD1TZEUM76
SOLIDWORKS: https://drive.google.com/drive/folders/1cqIBugpexhk7zoOh13YJuDqX04W12R3Y

Sub-team folders inside the Mechanical folder:
- Conquistadors: https://drive.google.com/drive/folders/1-N154LxBfmxJU8Cz5WTFKkoVAxI1Gutl
- Hip-to-Knee Mechanical Design: https://drive.google.com/drive/folders/18588fo7UQuo68TrtYW9ZAdcWz2FaoHSn
- Kit-Kat: https://drive.google.com/drive/folders/1XF-sLztf0rqBe9-xesQuOoOimf46Rgle

Access is limited to EXO members. If the link says you need access, use Request access or ask your team lead.

## Safety

1. No powered actuator moves until the bench stop path has been demonstrated and the Project Leads have confirmed it.
2. Nobody wears any part of the device, including the battery belt, until the Project Leads confirm written approval.
3. No on-body sensor data, and no data from anyone wearing part of the device, goes into Drive or GitHub.
4. No lithium-ion pack assembly until a reviewed build procedure exists.
5. Lab work in ENG 208 requires the lab safety courses to be complete.
6. Never commit passwords, tokens, keys, or Wi-Fi credentials. Use an ignored file and a committed example file.
