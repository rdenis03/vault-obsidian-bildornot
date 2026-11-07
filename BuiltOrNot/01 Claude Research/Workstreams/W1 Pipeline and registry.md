---
type: workstream
id: W1
confidence: medium
datasets: [w1_registry]
hypotheses: [H7, H8]
tests: [T5]
source_run: 2026-11-06
tags: [claude-research]
---
**Question.** How big is the solar and BESS pipeline, who holds it, and how far has it moved?

## Registry
- The government's 25 Apr 2026 list covers more than 1,400 ATRs held by more than 1,000 holders, with planned capacity above 80,000 MW, consolidated by Transelectrica from all operators' data ([[Sources#^S4|S4]], [[Sources#^S5|S5]]).
- The 1 MW threshold applies per holder, not per ATR, and the list is a selection, not exhaustive ([[Sources#^S4|S4]], [[Sources#^S5|S5]]).
- 76% of ATR-holding firms had zero turnover in 2024; 37 had turnover above RON 100 million ([[Sources#^S5|S5]]).
- Columns: ATR number and date, holder, CUI, MW, county, operator, stage, estimated commissioning date (mainly distribution rows), and audit columns naming the source spreadsheet. No locality, plot or coordinates ([[Sources#^S2|S2]]).
- CUI is the join key to company registries, CfD lists and deal notes.
- Largest entries ([[Sources#^S2|S2]]):
  - West Power Investments SRL, 1,043.7 MW, Arad, connection contract signed. This is the Rezolv / Dama Solar AI holder ([[Sources#^S36|S36]]).
  - Bucovina Renewables SRL, 770.98 MW, Suceava.
  - Worldwide Solar Energy SRL, 750.35 MW, Constanța, ATR dated 2026-01-27.
- Data flag: duplicate CUI, see [[Conflicts#^C8]].

## Totals and funnel
- Totals disagree (>80,000 MW on 25 Apr; 91,118 MW and 1,530 projects on 1 Jun; >78,000 per ANRE). See [[Conflicts#^C1]].
- ANRE's secretary general said fewer than 8,000 of the 78,000 have a real chance ([[Sources#^S21|S21]]).
- **Funnel (strongest datapoint for H7).** ANRE's draft-order rationale (6 Mar 2026), operator data at 1 Jan 2026 ([[Sources#^S8|S8]], [[Sources#^S9|S9]]):
  - 49% of ATR projects had posted the 5% guarantee;
  - of those, 12% had signed connection contracts;
  - 3% also had building permits;
  - about 1% also had an AI.
- Forward view per operator data at 1 Jun ([[Sources#^S23|S23]], [[Sources#^S24|S24]]): 647 projects (30,366 MW) expected 2026–2035; 143 (9,147 MW) in advanced development; 36 (2,050 MW) slated for 2026.

## Connected in 2026
- Transelectrica, 20 Aug 2026: 2,514 MW connected in 2026 (PV 1,331, storage 663, wind 496, hydrocarbons 20, biogas 5 MW) ([[Sources#^S25|S25]]). The parts sum to 2,515 MW; the gap is rounding.
- The 2,500 MW mark was crossed when IS Părău (76.76 MW / 150.288 MWh) connected. Storage stood at 989 MW on 1 Aug ([[Sources#^S25|S25]]).
- Year-end expectation: about 1,000 MW of PV and wind and about 1,000 MW of storage, plus gas at Mintia and Iernut ([[Sources#^S25|S25]]).
- Storage reached 1,094 MW / 2,310 MWh on 1 Sep (press) ([[Sources#^S26|S26]]).

## CfD auctions
| Round | Solar | Wind | Average strike (solar / wind) | Sources |
|---|---|---|---|---|
| R1 (2024) | 11 winners, 432 MW | 10 winners, 1,096 MW | EUR 51 / 65 per MWh | ([[Sources#^S33\|S33]]) |
| R2 (Aug 2025) | 26 winners, 1,488 MW | 23 winners, 1,263 MW | EUR 40.35 / 73.89 per MWh | ([[Sources#^S28\|S28]], [[Sources#^S29\|S29]], [[Sources#^S32\|S32]]) |
| R3 (Dec 2025) | not stated | 315.8 MW (wind round) | not found | ([[Sources#^S35\|S35]]) |

- Lowest R2 solar bid: Baboia Solar Plant, EUR 35.77/MWh (Ogrezeni) ([[Sources#^S31|S31]]).
- Dama won two 260 MW phases ([[Sources#^S31|S31]]); target COD Sep 2028, long-stop Sep 2030 ([[Sources#^S36|S36]]).
- Round totals and Dama's strike price: see [[Conflicts#^C2]] and [[Conflicts#^C3]]. The ministry page was not reached.

## Grants
- OMV Petrom and CE Oltenia: 50/50 JV building four parks, about 550 MW, more than EUR 400M, about 70% from the Modernisation Fund ([[Sources#^S53|S53]]). COD and first tranche disagree between releases: [[Conflicts#^C6]], [[Conflicts#^C7]].
- Transelectrica's PNRR project: 11.25 MW PV and 19.10 MWh storage ([[Sources#^S27|S27]]).

## Not found
- 87.2 GW at 1 May 2026.
- ANRE AI and licence registers; grant beneficiary lists.
- The ministry's CfD results page.

## Data
[[w1_registry]] (26 rows: 23 ATR, 2 CfD, 1 grant). Related: [[W2 Geolocation]], [[H7 Matching ATRs to sites is painful]], [[Tests and gates#T5 Truth table]].
