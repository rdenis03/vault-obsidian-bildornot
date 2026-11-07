---
type: workstream
id: W2
confidence: low
datasets: [w2_locations]
hypotheses: [H7]
tests: [T5, V2, V5]
source_run: 2026-11-06
tags: [claude-research]
---
**Question.** Where is each ATR on the ground: locality, plot, coordinates?

## Findings
- **GEM Global Solar Power Tracker** (Feb 2026, CC BY 4.0) covers operating phases of 1 MW or more and pipeline phases above 20 MW ([[Sources#^S38|S38]]). The integrated power tracker had a Sep 2026 release ([[Sources#^S40|S40]]).
  - Example row: Roșiorii De Vede Teleorman solar project I, 9.4 MWac, 44.0024, 24.9510, location precision "exact" ([[Sources#^S39|S39]]).
  - Romania rows were not downloaded.
- **Developer pages** can give locality and permit stage, e.g. EMAS Consulting's Corbu (Olt, 42.9 MWp + 172 MWh, RTB Q3 2025) ([[Sources#^S87|S87]]).
- **Rătești** coordinates 44.7011, 25.1819 come from Wikipedia (tertiary) ([[Sources#^S94|S94]]).
- Only **APM environmental notices** and **PUZ registers** are likely to carry plot references. Neither was searched.

## How v1.1 uses this
- Truth table: geolocate through county environmental-agency notices and permits, starting with the 30 demo parks ([[Business model v1.1]], weak point 4).
- Baseline for V2 stage dates: TZ-SAM / Global Renewables Watch first-appearance date.

## Not done
- TZ-SAM, Global Renewables Watch, OSM Overpass.
- APM notices, PUZ registers.
- GEM Romania download.

## Data
[[w2_locations]] (5 rows; 2 with coordinates). Related: [[W1 Pipeline and registry]], [[Open work#^O2]], [[Open work#^O11]], [[Open work#^O14]].

## Update 2026-11-07
- TZ-SAM publishes solar-farm polygons above 500 kW each quarter, with an estimated construction date for over 80% of assets ([[Sources#^S105|S105]], [[Sources#^S110|S110]]). It can locate operating and recently built parks, but its licence is non-commercial ([[Conflicts#^C17]]).
- Sentinel-2 footprints can confirm a matched site; see [[Sentinel-2]].
