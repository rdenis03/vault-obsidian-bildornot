---
type: reference
title: "BuiltOrNot v1.1: refined business model and feasibility test"
date: 2026-11-06
author: denis
origin: https://claude.ai/artifact/9YHCLaLiSJRp1wM7PVx4vZ
verdict: go-with-six-changes
tags: [claude-research]
---
Condensed from the v1.1 review (6 Nov 2026). The full doc, with the T2 shadow chart and the T4 screening diagram, is at the `origin` link. Tests and kill criteria are in [[Tests and gates]]; the interview script is in the H notes. Sources B1–B6 are in [[Sources]].

## Verdict
**Go, with six changes.** Feasible as a Demo Day MVP and plausible as a small Romanian business. Three v1.0 assumptions fail: the capacity reference, per-site imagery tasking, and the timing of Start Alerts. Three changes sharpen who pays and for how long.

| # | Change | Why |
|---|---|---|
| 1 | Validate DC MWp against developer-reported MWp, not ANRE licensed MW | Licences are usually AC. At DC/AC 1.10–1.40, a method right to 4.4% scores 23.8% MAPE against AC and fails the 8% test |
| 2 | Never task Pléiades Neo per site. Sentinel-1/2 everywhere, monthly SPOT on active sites, Neo archive at 3 key dates | Monthly Neo tasking at a 100 km² minimum is about €2.4M a year; the ladder is about €29k |
| 3 | Start Alerts become Build Signals: paperwork events confirmed from space | EPC and module contracts are usually signed before fences and piles; the earlier signal is permits, connection contract, CfD award |
| 4 | Re-rank buyers: deal evidence for investors and advisers, a market-data feed for traders and IPP strategy; lenders through their technical advisers | They price a decision worth €0.6–1.2M (one avoided 20 MW paper project) and act after construction starts |
| 5 | Track batteries from day one, not from 2030 | 9.1 GW of storage holds building permits; containers are countable at 30–50 cm |
| 6 | Deadline Radar is the launch hook, not the business | The 12-month rule purges phantom projects by about 2027–28; what lasts is the dated record and evidence packs |

Two smaller corrections:
- **Measure modules as row length × known table depth.** Inferring tilt from cos β is fragile: half a pixel of width error moves tilt by 4° and area by 4%.
- **Competitors exist.** Kayrros, i-EM, GEOSAT and Lium monitor construction from space. The honest claim: nobody does it for Romania with the paperwork joined. See [[W6 Competition]].

## Keep from v1.0
- A problem with money and a clock: 91.1 GW of valid ATRs against about 3.5 GW of utility-scale solar ever built; the May 2026 rules price the question "is it really being built?"
- One dataset, many buyers: built once, sold several times.
- Physics makes numbers checkable: every figure traces to an image date, a formula and its assumptions.
- Free first, sharp only where something changed: Sentinel screens, paid VHR only on changed sites.
- The moat is the truth table (ATR, permits, owner, deals per park), not panel detection, which is commodity (TZ-SAM, Global Renewables Watch).
- Legal care: observations, never accusations; county aggregates only in public; a correction channel for owners.
- Kill criteria and stage gates G0–G4 (G0 and G4 are defined in v1.0, which is not in this vault).
- The worked example recomputes: tilt 25.0°, module area 231,724 m², 51.0 MWp ± 5.7%.

## Ten weak points and fixes
| # | Weak point | Fix |
|---|---|---|
| 1 | MWp checked against licensed (AC) capacity | Reference = developer- or EPC-reported MWp plus module counts; report DC/AC as an output |
| 2 | Verification relies on tasking (~€3,000 per new Neo image at 100 km² vs a €1,500–3,000 report) | Archive by default (~€90 per site-date at UP42's 5 km² minimum); tasking as a pass-through; ask sellers for clustered AOIs. See [[Conflicts#^C11]] |
| 3 | Start Alerts reach suppliers too late (H) | Lead with paperwork signals confirmed by satellite; sell site-stage alerts to post-start buyers |
| 4 | The truth table is the slowest part: the ATR list has no coordinates or substation | Geolocate through county environmental-agency notices and permits; start with the 30 demo parks; budget a person, not a script |
| 5 | Screening floods the review queue: single-date bare-soil test ~0.1% precision | Stack filters (2-pass persistence, distance to ATR substations, ≥5 ha, linear roads or fences, SAR change): ~43% precision, ~18 candidates a month |
| 6 | Pile counts are fragile: 0.12–0.15 m piles fill 40–50% of a 30 cm pixel; 220–480 piles/MW by layout (v1.0 assumed 250) | Measure piled-area fraction at native 30 cm in Feb–Mar or Oct–Nov; counts are a stretch goal |
| 7 | Deadline Radar promises calibrated odds from too few completed builds | Ship bands first ("approved, no visible work 9+ months"); odds only after held-out calibration |
| 8 | Small market (€1.6–4.1M a year); 2028 needs 20 of ~110 reachable accounts; the moat does not travel | Price for retention; expand to BESS and wind in Romania, then countries with public ATR lists |
| 9 | Competitors are closer than v1.0 says | Position on Romania, the paperwork join, BESS and accepted evidence; watch Kayrros for a CEE entry |
| 10 | Lenders do not replace site visits; technical advisers visit monthly and sign drawdowns | Sell to technical advisers as a between-visits tool and portfolio view |

H marks a hypothesis to test in interviews.

## The model
**Positioning.** For investors, their advisers and energy-market analysts in Romania: the independent, dated record of what is being built on every approved solar and battery site (stage, DC MWp and the paperwork behind it). Registries say what was approved; free solar maps say what is finished; BuiltOrNot shows what happens in between, packaged as evidence.

### Who pays, ranked
| Rank | Segment | Decision it changes | Product |
|---|---|---|---|
| 1 | Investors, IPP M&A and strategy, deal lawyers and advisers (~40 accounts) | Buy, price or walk away; release payment at a milestone | Pro + Evidence Packs |
| 2 | Traders, market analysts, energy data vendors (~15 + 2–3 vendors) | How much solar and storage arrives next quarter | Build-out Feed |
| 3 | Lenders' technical advisers (~12) | Certify a drawdown between site visits | Evidence Packs, monthly |
| 4 | Post-start sellers: O&M, insurers, BESS retrofit, grid subcontractors | Whom to pitch this month | Build Signals (test segment) |
| 5 | Module, tracker and EPC sellers | Whom to pitch before procurement | Paperwork signals only (H) |
| 6 | Transelectrica, distribution operators, ANRE | Which connections materialise; which ATRs to enforce | Grant-funded pilot (ESA Business Applications or ROSA) |

### Products
| Product | Replaces | Gives | Price (H) |
|---|---|---|---|
| Public map, quarterly "Approved vs Built" | same | County aggregates, no company names | Free |
| Build Signals | Start Alerts | Paperwork events plus satellite confirmation of start, stall, modules complete | €400–800/month |
| Pro | same | Project pages, truth table, stage history since 2021, stall and deadline bands, 6 packs a year | €2,000–3,500/month |
| Evidence Pack | Verification report | Dated stage, piled-area fraction, DC MWp ± error, method, archive imagery | €1,500–2,500 per pack; tasking at cost + 20% |
| Build-out Feed | MWp Meter | Monthly MWp and MWh under construction by county, "built, awaiting energisation", expected COD month | €10–25k/year direct; revenue share via vendors |
| BESS Tracker | new (was 2030) | Container counts to an MWh range | Included in Pro and Feed |

### Data ladder
| Step | Source | Cadence | Cost per site-date |
|---|---|---|---|
| Screen | Sentinel-2 L2A 10 m + Sentinel-1 GRD via CDSE / openEO | Every pass | Free |
| Confirm and stage | SPOT 1.5 m archive (or PlanetScope 3 m; quote needed) | Monthly at active sites | ~€2 |
| Measure | Pléiades Neo 30 cm archive | 3 key dates per build: piles, tables, modules complete | ~€90 |
| Evidence on demand | Pléiades Neo tasking | When a customer needs a date | ~€3,000, customer pays |
| Hackathon only | Airbus via ESA TPM (research use); KOMPSAT-3A archive via AIM Space as backup | As available | Free under research terms |

Canvas changes: key partners gain lenders' technical advisers, energy data vendors and county environmental agencies (as a data source); channels gain data vendors; revenue order is Pro, Evidence Packs, Feed licences, Signals.

## Feature triage for Demo Day
- **Build (11):** national map with county aggregates; project page with time-lapse; stage classifier for stages 1, 3, 4, 5 (site, tables, modules, power blocks); pile stage as piled-area fraction; MWp as row length × table depth; MWp validation against developer MWp with a fenced-area baseline; truth table (gov.ro import, 30 hand-linked parks, review queue); BESS container detection (5 sites); "built, awaiting energisation" flag (508 MW sat in this state in July 2026); "unsure" class with confidence per stage; evidence change log.
- **Mock-up (2):** Build Signals with 3 real examples; correction channel.
- **Stretch (2):** pile counts from HD15 as a cross-check; trader forecast beyond county aggregates.
- **Not yet (4):** DC/AC as an output; Deadline Radar odds; progress index Σwᵢcᵢ; public API, SSO, multi-tenant.

## Scorecard against course Modules 1–4
v1.0 passes 4 of 15 checks, partly passes 7, fails 4. All four failures are about honest testing:
- **Fail:** precision at low prevalence (report precision per review queue); split matching deployment (leave-one-park-out for stages, county blocks for detection); reference of the same quantity (developer-reported MWp, not AC licences); calibrated probabilities before calling them risk (bands until about 100 completed builds).
- **Partly:** simplest instrument (HD15 counts as a check only); real gap (name competitors); free data first (tasking at cost, archive by default); licence chain (Earth Engine free tier is non-commercial, so production runs on CDSE / openEO); thresholds and look-alikes (add ploughing and harvest); beat a baseline (fenced area × MWp/ha; TZ-SAM / GRW first appearance); fine-print checks (query the archive for the 20 test parks in week 1).

## Pitch opening line
"Romania holds 91 GW of grid approvals, but all the utility-scale solar it has ever built is about 3.5 GW. We show which approvals are turning into steel, panels and batteries: a dated, checkable record for every site."

> [!warning] Figures in this note without a source ID (3.5 GW built, 9.1 GW storage with permits, 508 MW awaiting energisation) come from v1.0's sources [1]–[30], which are not in this vault. See [[Conflicts#^C15]].
