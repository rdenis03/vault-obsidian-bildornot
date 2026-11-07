---
type: workstream
id: W8
confidence: low to medium
datasets: [w8_parameters]
hypotheses: []
tests: [T1, T2, V1, V3]
source_run: 2026-11-06
tags: [claude-research]
---
**Question.** Which physical parameters turn imagery into MWp, MWh and stage, and what do Romanian parks actually show?

## DC/AC ratio
| Park | DC/AC | Sources |
|---|---|---|
| Horia 2 | 1.089 | ([[Sources#^S51\|S51]]) |
| Iratosu | 1.208 | ([[Sources#^S50\|S50]]) |
| EDPR park | 1.230 | ([[Sources#^S89\|S89]]) |
| Dama Solar | 1.188–1.245 | ([[Sources#^S36\|S36]], [[Sources#^S37\|S37]]) |
| Titu | 1.274 | ([[Sources#^S41\|S41]]) |
| Ogrezeni | 1.404–1.425 | ([[Sources#^S52\|S52]], [[Sources#^S91\|S91]]) |

Observed range 1.089–1.425 is wider than the 1.10–1.40 v1.1 used to show why AC licences fail as a reference. The conclusion holds; the error band is slightly wider.

## Land use (ha per MWp, computed)
| Park | Calculation | ha/MWp | Sources |
|---|---|---|---|
| Dama Solar | >1,000 ha / ~1,240 MWp | ≥ 0.81 | ([[Sources#^S36\|S36]]) |
| Horia 2 | >349 ha / 293.26 MWp | ≥ 1.19 | ([[Sources#^S51\|S51]]) |
| Ișalnița (OMV Petrom) | 120.13 ha / ~89 MWp | 1.35 | ([[Sources#^S55\|S55]]) |
| Aricești (Engie) | 57 ha / 37.2 MWp | 1.53 | ([[Sources#^S46\|S46]]) |

This range feeds the V1 baseline (fenced area × typical MWp/ha).

## Other derived values (ESTIMATE, computed)
- **Titu module wattage:** 54.28 MWp / 88,270 modules ≈ 615 W ([[Sources#^S41|S41]]).
- **Titu inverter size:** 42.60 MWac / 142 inverters ≈ 300 kW each ([[Sources#^S41|S41]]).
- **BESS duration:**
  - IS Părău: 150.288 MWh / 76.76 MW ≈ 1.96 h ([[Sources#^S25|S25]]).
  - Renalfa Arad BESS: 800 MWh / 400 MW = 2.0 h ([[Sources#^S66|S66]]).

## v1.1 assumptions still unverified
- Piles per MW: 220–480 by layout (v1.0 assumed 250).
- Pile width 0.12–0.15 m.
- Table depth by layout (1P, 2P, 3L), used for row length × table depth.

## Not found
Piles per MW, pile height above ground, table depth (1P or 2P), MWh per BESS container.

## Data
[[w8_parameters]] (17 rows). Related: [[W3 Reference parks and deals]], [[Tests and gates#T1 DC capacity from VHR]], [[Tests and gates#T2 Pile stage]].
