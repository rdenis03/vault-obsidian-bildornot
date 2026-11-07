---
type: reference
added: 2026-11-07
workstreams: [W2, W4, W6, W8]
tests: [T3, T4, T7, T11, V1, V2, V4]
tags: [claude-research, sentinel-2]
---
The team's imagery source. This note covers what Sentinel-2 can and cannot show for BuiltOrNot, how to get it for free, and what that means for the v1.1 plan. Sources S96–S110 were added on 7 Nov 2026.

## Bottom line
- **Sentinel-2 sees the start and the finish of a build, not the middle.**
  - It sees site clearing (stage 1) and modules (stage 4).
  - It does not see piles or power blocks (stages 2 and 5).
  - Tables (stage 3) are at best "unsure".
- **Its value is dates.** Revisit is 2–3 days at mid-latitudes with two satellites ([[Sources#^S99|S99]]), and a third satellite (2A) is extended to the end of 2027 ([[Sources#^S98|S98]]). Clear-sky frequency over Romania is not yet measured ([[Open work#^O16]]).
- **MWp from Sentinel-2 is a range, not ±8%.** Area × MWp/ha is exactly v1.1's baseline, so V1 cannot pass as written with Sentinel-2 alone. See [[#MWp from Sentinel-2]].
- **Free, full and open, with attribution.** The licence allows reproduction, distribution, adaptation and combination with other data, and sets no non-commercial limit ([[Sources#^S102|S102]]). TZ-SAM, built on 10 m imagery, is **non-commercial** (CC BY-NC 4.0) ([[Sources#^S105|S105]], [[Sources#^S106|S106]]).

## The data
| Item | Fact | Sources |
|---|---|---|
| Satellites | 2B and 2C operational; 2C replaced 2A on 2025-01-21. 2A moved 36° from 2B and resumed observations on 2025-03-13 | ([[Sources#^S96\|S96]], [[Sources#^S97\|S97]], [[Sources#^S99\|S99]]) |
| 2A extension | Continues until 2027-12-31, under the operating scenario introduced in 2025 | ([[Sources#^S98\|S98]]) |
| Revisit | 5 days with two satellites at the equator; 2–3 days at mid-latitudes. 2A adds passes 2 days after 2B and 1 day after 2C | ([[Sources#^S97\|S97]], [[Sources#^S99\|S99]]) |
| Bands | 13 bands: four at 10 m (B2 blue, B3 green, B4 red, B8 NIR), six at 20 m (red edge, B8A, B11 and B12 SWIR), three at 60 m | ([[Sources#^S99\|S99]], [[Sources#^S103\|S103]]) |
| Swath | 290 km | ([[Sources#^S99\|S99]]) |
| Products | L1C top-of-atmosphere; L2A surface reflectance with scene classification (SCL); L3 quarterly mosaics | ([[Sources#^S99\|S99]]) |
| Archive | L1C from 2015; Earth Engine L2A harmonized from 2017-03-28 | ([[Sources#^S99\|S99]], [[Sources#^S103\|S103]]) |
| Offset | From processing baseline 04.00 (after 2022-01-25), values carry a +1000 offset. Earth Engine's HARMONIZED collections remove it; elsewhere, check before comparing scenes | ([[Sources#^S103\|S103]]) |
| Licence | Free, full and open: reproduce, distribute, adapt, combine. Attribution required | ([[Sources#^S102\|S102]]) |

**Attribution on every output:** "Contains modified Copernicus Sentinel data [year]" ([[Sources#^S102|S102]]).

## Free access
| Route | Free allowance | Notes | Sources |
|---|---|---|---|
| CDSE openEO | 10,000 credits a month per user (a temporary boost); 12 requests a minute; 2 concurrent | A 10 ha, one-index batch job cost 8.2 credits, so about 1,200 such jobs a month | ([[Sources#^S100\|S100]], [[Sources#^S101\|S101]]) |
| CDSE Sentinel Hub | 10,000 processing units and 10,000 requests a month; 300 a minute | Resets monthly; no rollover; over quota means slower service | ([[Sources#^S100\|S100]]) |
| CDSE downloads (S3, OData) | 12 TB per rolling 30 days; 4 connections at 20 MB/s | | ([[Sources#^S100\|S100]]) |
| Earth Engine | `COPERNICUS/S2_SR_HARMONIZED` + `GOOGLE/CLOUD_SCORE_PLUS/V1/S2_HARMONIZED` | Free tier is non-commercial; fine for the hackathon, not for production | ([[Sources#^S103\|S103]], [[Sources#^S104\|S104]], [[Sources#^S77\|S77]]) |

- Quotas are per user account: each teammate gets their own.
- Whether a free CDSE account may run a commercial service: NOT FOUND. Extended quotas under commercial terms exist ([[Sources#^S100|S100]]).
- v1.1's 10,000 openEO credits a month is confirmed; Earth Engine's 150 EECU-hours a month is still not confirmed.

## What Sentinel-2 shows, by build stage
| Stage (v1.1) | Visible at 10 m? | Signal | Main look-alikes | Basis |
|---|---|---|---|---|
| 1 Site | **Yes, as change** | NDVI falls, BSI rises, and the change persists over clear passes | Ploughing, harvest | v1.1 T4; persistence rule ESTIMATE |
| 2 Piles | **No** | A 0.12–0.15 m pile is 1.2–1.5% of a pixel's width | — | computed |
| 3 Tables | **Unsure** | Texture and reflectance shift before modules | Early module rows | ESTIMATE; v1.1: rows resolve at 1.5 m |
| 4 Modules | **Yes** | PV signature; segmentation works on RGB alone | Plastic greenhouses (remove with a greenhouse index) | ([[Sources#^S108\|S108]], [[Sources#^S109\|S109]]) |
| 5 Power blocks | **No** (not as objects) | Inverter and MV stations are smaller than a pixel | — | ESTIMATE; v1.1: visible at 30–50 cm |
| BESS | **Footprint only, no count** | A cleared pad with a bright block | Warehouses, car parks | ESTIMATE; v1.1: containers countable at 30–50 cm |
| Energised | **No** | Not visible from optical | — | Use Transelectrica and ANRE records |

**Reported accuracy for PV detection:**
- GloSoFarID: 13,703 Sentinel-2 samples, 2021–2023; best model 96.47% IoU and 98.2% F-score; U-Net 87.8% F-score ([[Sources#^S108|S108]]).
- Italy (Ronchetti et al. 2025, RGB U-Net): user's accuracy 63–100% in one region, F1 around 60% in another. The authors note that small plants are lost to mixed pixels ([[Sources#^S109|S109]]).

**Size check (computed):** a 1 MW park at 0.81–1.53 ha/MWp covers 0.8–1.5 ha, or 80–150 Sentinel-2 pixels. Every project in the ATR list (≥ 1 MW per holder) is many pixels wide.

## v1.1 Demo Day features with Sentinel-2 only
| Feature (v1.1 Build or Mock-up) | With Sentinel-2 alone |
|---|---|
| National map with county aggregates | Yes |
| Project page with time-lapse | Yes, at 10 m |
| Stage classifier, stages 1, 3, 4, 5 | 1 and 4 yes; 3 unsure; 5 no |
| Pile stage (piled-area fraction) | No: needs native 30 cm |
| MWp as row length × table depth | No: needs VHR. Sentinel-2 gives an area-based range |
| MWp validation against developer MWp | Baseline only; see below |
| Truth table | Yes: paperwork, not imagery |
| BESS container detection | Footprint only, no MWh range |
| "Built, awaiting energisation" flag | Partly: modules complete is visible; power blocks are not |
| "Unsure" class with confidence per stage | Yes, and needed more often |
| Evidence change log | Yes: cite tile, date and product |
| Build Signals (mock-up) | Yes: a paperwork event plus Sentinel-2 confirmation of start or modules complete |
| Correction channel (mock-up) | Yes |

**V2 (stage dates within one month for stages 1, 4 and 5):**
- Stages 1 and 4 are plausible with Sentinel-2, if enough clear scenes exist ([[Open work#^O16]]).
- Stage 5 is not visible.

## MWp from Sentinel-2
Sentinel-2 can measure the footprint; it cannot resolve rows. MWp then equals area × density, which is v1.1's V1 baseline. The density in our four parks spans almost 2× (computed from [[W8 Technical parameters]]):

| Park | ha/MWp | MWp per ha |
|---|---|---|
| Dama Solar | ≥ 0.81 | ≤ 1.23 |
| Horia 2 | ≥ 1.19 | ≤ 0.84 |
| Ișalnița (OMV Petrom) | 1.35 | 0.74 |
| Aricești (Engie) | 1.53 | 0.65 |

So a 50 ha site reads as anything from about 33 to 62 MWp (computed). Until density is calibrated by layout on the V1 parks, report MWp as a range and drop the ±8% claim. To keep V1 as a test, one option is to redefine it as "Sentinel-2 footprint × calibrated density beats a single national density". That is a decision for the team, not made here.

## Working recipe
1. **Collection.**
   - CDSE openEO: `SENTINEL2_L2A`.
   - Earth Engine: `COPERNICUS/S2_SR_HARMONIZED` ([[Sources#^S103|S103]]).
2. **Cloud mask.**
   - Earth Engine: Cloud Score+ `cs` ≥ 0.60 (0.50–0.65 generally works) ([[Sources#^S104|S104]]).
   - CDSE: drop SCL classes 3 (cloud shadow), 8–9 (cloud), 10 (cirrus), and 11 (snow) in winter ([[Sources#^S103|S103]]).
3. **Indices.**
   - NDVI = (B8 − B4) / (B8 + B4).
   - BSI = ((B11 + B4) − (B8 + B2)) / ((B11 + B4) + (B8 + B2)).
4. **Screen.** Flag cells where NDVI falls and BSI rises, and keep only changes that persist over 2 clear passes. Then apply v1.1's stacked filters: distance to ATR substations, ≥ 5 ha, linear roads or fences, and SAR change.
5. **Review.** Each flagged change becomes a Candidate note (team template). Candidate verdicts give V4's precision directly.
6. **Confirm.** A true start becomes a Project record. Its physical-evidence rows cite tile, date, product and clear-sky score.
7. **Cloudy weeks.** Sentinel-1 SAR change, as in v1.1.

## Datasets built on 10 m imagery
- **TZ-SAM** (TransitionZero):
  - Covers solar farms above 500 kW, released quarterly from 2024Q4 ([[Sources#^S105|S105]]).
  - Publishes polygons, estimated capacity, and an estimated construction date for over 80% of assets ([[Sources#^S110|S110]]).
  - The construction date is bracketed by the image in which the plant is first seen built ([[Sources#^S106|S106]]).
  - Licence: **CC BY-NC 4.0** ([[Sources#^S105|S105]], [[Sources#^S106|S106]]). Fine as V2's research baseline; **not usable in a paid product** without TransitionZero's permission ([[Open work#^O17]]).
- **GloSoFarID:** a global Sentinel-2 solar-farm training set ([[Sources#^S108|S108]]). Licence not stated in the paper.
- **Precedent:** COTESA built a proof of concept for EDP, supported by EUSPA, that detects PV construction start and progress from Sentinel-2 in Portugal (15 km², builds 2022–24). It reports the method works above a 150 m² project size ([[Sources#^S107|S107]]). See [[W6 Competition]].

## Not found / not done
- Clear-sky Sentinel-2 observations per month over Romanian test parks: NOT DONE ([[Open work#^O16]]).
- Whether CDSE free accounts may serve a commercial product: NOT FOUND.
- Earth Engine EECU-hour quota for the free tier: NOT FOUND.
- A tested Sentinel-2 signal for stage 3 (tables): NOT FOUND.
