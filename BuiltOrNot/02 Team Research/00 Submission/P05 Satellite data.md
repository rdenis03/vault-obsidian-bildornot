---
type: section
part: P05
title: "Satellite data"
time: "45 sec"
track: "both"
status: draft
owner: unassigned
updated: 2026-11-07
---
**Needs:** The exact datasets: mission, product level, resolution, revisit, where you get them, what each shows. Other data. Why satellite data is the right source.
**Rule:** List exact datasets and where they come from.

## Draft
| Mission and product | Resolution | Revisit | Access | Used for |
|---|---|---|---|---|
| Sentinel-2 L2A | 10 m (blue, green, red, NIR); 20 m SWIR | 2–3 days at mid-latitudes ([[Sources#^S99\|S99]]); extra 2A passes to end-2027 ([[Sources#^S98\|S98]]) | CDSE (openEO, Sentinel Hub); Earth Engine for prototyping ([[Sources#^S100\|S100]], [[Sources#^S103\|S103]]) | Site clearing, modules, dates |
| Sentinel-1 GRD | 10 m pixels, C-band, VV + VH | 6 days ([[Sources#^S111\|S111]]) | CDSE; Earth Engine | Change in cloudy weeks |
| Cloud Score+ | 10 m | Per Sentinel-2 scene | Earth Engine ([[Sources#^S104\|S104]]) | Cloud masking |

- **Other data:**
  - Government ATR list (holder, CUI, MW, county, stage) ([[Sources#^S2|S2]]).
  - Transelectrica connection reports ([[Sources#^S25|S25]]).
  - ANRE Order 15/2026 ([[Sources#^S11|S11]]) and CfD results ([[Sources#^S31|S31]]).
  - Developer-reported MWp for validation ([[Sources#^S41|S41]]).
- **Why satellite data:** an independent, dated view of every site every few days, free and open ([[Sources#^S102|S102]]). Registries say what was approved; imagery shows what is built.
- Credit line: "Contains modified Copernicus Sentinel data 2026" ([[Sources#^S102|S102]]).

## Open
- [ ] Confirm Earth Engine is used only for the hackathon (its free tier is non-commercial).

## Evidence
[[Sentinel-2]] · [[W4 Imagery]]
