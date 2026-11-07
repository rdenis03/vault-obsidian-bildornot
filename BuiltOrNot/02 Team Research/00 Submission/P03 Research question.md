---
type: section
part: P03
title: "Research question"
time: "45 sec"
track: "Scientific Research only"
status: draft
owner: unassigned
updated: 2026-11-07
---
**Needs:** What is known (2–3 key references); what is not known; one focused question; the hypothesis and why.
**Rule:** Only if the track is Scientific Research. Enterprise Software teams leave this part out.

## Draft
- **What is known:**
  - Solar farms are detectable in 10 m Sentinel-2 imagery: TZ-SAM, GloSoFarID, and Ronchetti et al. 2025 ([[Sources#^S106|S106]], [[Sources#^S108|S108]], [[Sources#^S109|S109]]).
  - Construction start has been detected from Sentinel-2 in a Portuguese proof of concept ([[Sources#^S107|S107]]).
- **What is not known:** whether Sentinel-2 time series can date the construction stages of utility solar and battery sites in Romania, and tie them to grid-approval paperwork, well enough to separate real projects from paper ones.
- **Our research question:** Can Sentinel-2 time series date site clearing and module completion at Romanian utility solar parks to within one month?
- **Hypothesis:**
  - Yes for site clearing and modules, where enough clear observations exist each month, because both change reflectance over hectares.
  - No for piles and power blocks, which are smaller than a pixel.

## Open
- [ ] Keep only if the track is Scientific Research.
- [ ] Set "enough clear observations" from the clear-sky counts ([[Open work#^O16]]).

## Evidence
[[Sentinel-2]] · [[Tests and gates#V2 Stage dating on 10 parks]]
