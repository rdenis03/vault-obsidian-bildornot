---
type: overview
source_run: 2026-11-06
updated: 2026-11-07
tags: [claude-research]
---
Two Claude outputs from 6 Nov 2026 make up this folder:

1. **[[Business model v1.1]]**: the feasibility review of BuiltOrNot v1.0. Verdict: go, with six changes.
2. **Evidence pack**: desk research on the Romanian solar and BESS pipeline across eight workstreams (W1–W8), with 12 datasets in `Data/` and 91 logged sources in [[Sources]].

The evidence-pack run did not meet its own effort rules (15 searches and 8 primary pages per workstream, plus saturation). Every gap is marked NOT FOUND or NOT DONE rather than filled. Label meanings are in [[CLAUDE]].

## Bottom line
- **Paperwork exists, location does not.** The ATR list gives holder, CUI, MW, county, operator and stage for every project, but no locality, plot or coordinates ([[Sources#^S2|S2]], [[Sources#^S5|S5]]). Mapping ATRs to sites (T5) is manual work.
- **The rules set the clock.** ANRE Order 15/2026 requires an establishment authorisation (AI) within 12 months of the connection contract. For contracts already signed the deadline falls around 2027-05-25 (ESTIMATE) ([[Sources#^S11|S11]], [[Sources#^S15|S15]]). Dated progress evidence matters most in this window.
- **Imagery is cheap per km²; the minimum order decides the cost.** Pléiades Neo archive lists at USD 22.50/km² at three resellers, with minimums from 5 to 100 km² ([[Sources#^S67|S67]], [[Sources#^S69|S69]], [[Sources#^S71|S71]]). Archive revisit counts (T7) were not done.
- **V1 is far from met.** Two commissioned parks with both MWp and MWac published, against the 20 needed.

## Workstreams
| ID | Note | Confidence | State in one line |
|---|---|---|---|
| W1 | [[W1 Pipeline and registry]] | Medium | ATR list parsed from a mirror (~200 rows); totals conflict |
| W2 | [[W2 Geolocation]] | Low | GEM coverage known; APM, PUZ, OSM not run |
| W3 | [[W3 Reference parks and deals]] | Low (V1), Medium (deals) | 2 of 20 V1 parks; 10 deals with advisers |
| W4 | [[W4 Imagery]] | Medium (prices), none (archive) | 20 price rows; T7 not done |
| W5 | [[W5 Market accounts]] | Medium (names), Low (spend) | 44 account rows; no traders or insurers named |
| W6 | [[W6 Competition]] | Low | 3 profiled; Lium, i-EM, GEOSAT, Imageryst not searched |
| W7 | [[W7 Regulation]] | High (Order 15/2026) | Rules and dates set; primary texts not opened |
| W8 | [[W8 Technical parameters]] | Low to Medium | DC/AC 1.09–1.43; pile and table data not found |

## Hypotheses
| ID | Note | Desk status (6 Nov) |
|---|---|---|
| H1 | [[H1 Buyers pay for dated progress evidence]] | Weakly supported |
| H2 | [[H2 Alerts come too late for EPC and module sellers]] | Supported for EPC; module timing not found |
| H3 | [[H3 Post-start sellers want completion signals]] | Mixed |
| H4 | [[H4 Traders want MWp under construction by month]] | Partly supported |
| H5 | [[H5 Technical advisers would use packs between visits]] | Not tested |
| H6 | [[H6 Pro costs less than current substitutes]] | No evidence found |
| H7 | [[H7 Matching ATRs to sites is painful]] | Supported indirectly |
| H8 | [[H8 Battery build-out matters as much as solar]] | Contradicted at aggregate level; open per project |

## Key dates
| Date | Event |
|---|---|
| 2026-11-07 | Ideathon interviews (questions in each H note) |
| 2026-11-07 to 13 | Week 1 checklist, now in [[Open work]] |
| 2026-11-12, 19, 26; 12-03, 12-10 | Masterclass workshops |
| TBC | Intermediate milestone (date from the organisers) |
| 2026-12-11 | Demo Day: submission of P01–P12 with README and demo video ([[Submission]]); 34 days after 7 Nov |
| ~2027-05-25 | AI deadline for connection contracts in force under Order 15/2026 (ESTIMATE) ([[Sources#^S11\|S11]]) |
| 2027-04 | Gate G1: someone pays beyond free data, or stop the subscription business |
| 2027-09 | Gate G2: at least 3 usable Neo archive dates per build |
| 2028-06 | Gate G3: renewal intent and lender-adviser use |
| 2028-09 | Dama Solar target COD; long-stop 2030-09 ([[Sources#^S36\|S36]]) |

## Read next
- [[Conflicts]]: figures that disagree, and which to use.
- [[Open work]]: everything still to do, unassigned.
- [[Tests and gates]]: T1–T11, V1–V6 and the kill criteria.
- [[Sentinel-2]]: the team's imagery; what it can and cannot show, free access, and what it changes in v1.1 (added 2026-11-07).

## Coverage of the 6 Nov run
| Workstream | Searches | Pages opened | Files parsed | Rows | Saturated |
|---|---|---|---|---|---|
| W1 | 6 | 2 (S2, S25) | 2 PDFs, partial | 26 | No: budget exhausted |
| W2 | 1 | 0 | 0 | 5 | No: APM, PUZ, OSM not run |
| W3 | 6 + subagent ~12 | 1 (S41) | 0 | 13 parks, 10 deals | No |
| W4 | 2 | 0 | 0 | 20 prices, 0 counts | No |
| W5 | shared with W3 | 0 | 0 | 44 | No |
| W6 | 2 | 0 | 0 | 7 | No |
| W7 | 1 | 0 (S10, S11 blocked) | 0 | 10 | No |
| W8 | derived | 0 | 0 | 17 | No |

## Run assumptions
- A1. The v1.1 artifact could not be read during the run. Resolved 7 Nov: it is [[Business model v1.1]].
- A2. The gov.ro ATR PDF is blocked by robots.txt; the presshub.ro mirror with identical columns was used, not hashed or checked against the original ([[Sources#^S1|S1]], [[Sources#^S2|S2]]).
- A3. ATR MW is approved export power, recorded as `mw_ac`, not DC.
- A4. Technology is recorded only where the source labels it (Distribuție Energie Oltenia: FOTOVOLTAIC; CEM = mixed; IS = storage).
- A5. No files were saved, hashed or downloaded raw, and no Overpass query was run. sha256 reads NOT COMPUTED.
- A6. In the workstream CSVs the `url` column holds the source ID; full URLs are in `sources.csv`.
