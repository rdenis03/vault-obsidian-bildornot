---
type: section
part: P06
title: "Method or architecture"
time: "45 sec"
track: "optional"
status: draft
owner: unassigned
updated: 2026-11-07
---
**Needs:** The steps from data to result, how they are validated, and the main tools.
**Rule:** Software teams: how data flows from source to user interface.

## Draft
| Data | Pre-processing | Analysis or model | Validation | Results or interface |
|---|---|---|---|---|
| Sentinel-2 L2A and Sentinel-1 GRD, 2021–2026; 2–3 screening counties plus 30 demo sites | Cloud Score+ `cs` ≥ 0.60 or SCL mask; clip to sites and counties | NDVI and BSI change that persists over 2 clear passes; stacked filters; PV segmentation (U-Net baseline); stage dating | Stage dates against image or developer dates (V2); two-person site matching (V5); precision in a held-out county (V4); split by site | County map, project pages with time-lapse, evidence log |

Tools: Python, openEO (CDSE), Google Earth Engine, QGIS. Web stack: to choose.

## Open
- [ ] Choose the web stack.
- [ ] Start the repo ([[Open work#^O13]]).

## Evidence
[[Sentinel-2#Working recipe]] · [[Tests and gates]]
