---
type: workstream
id: W4
confidence: medium (prices), none (archive counts)
datasets: [w4_prices, w4_archive_counts]
hypotheses: []
tests: [T6, T7, T11]
source_run: 2026-11-06
tags: [claude-research]
---
**Question.** What does VHR imagery over Romanian sites cost, what is the minimum order, and how often does the archive already hold a usable scene?

## Pléiades Neo list prices
| Seller | Archive USD/km² | Tasking USD/km² | Minimum | Sources |
|---|---|---|---|---|
| LAND INFO | 22.50 (HD15 26.25) | 32.50 (HD15 36.25) | 25 km² archive; tasking not found | ([[Sources#^S67\|S67]]) |
| Apollo Mapping | 22.50 | not found | 25 km² archive | ([[Sources#^S70\|S70]]) |
| SkyWatch | 22.50 (HD15 25.00) | 32.50 | 5 km² | ([[Sources#^S71\|S71]]) |
| UP42 | from 1,800 credits/km² | from 2,600 credits/km² | archive priced as per 5 km²; tasking as per 100 km² | ([[Sources#^S69\|S69]]) |

- LAND INFO's Dec 2024 sheet lists a 30% education discount and an 80% high-demand uplift in some geographies ([[Sources#^S68|S68]]).
- UP42 offers 10-minute delivery priced as per 0.1 km² ([[Sources#^S69|S69]]).
- Sentinel Hub: EUR 100 per 11.76 km² quota package (about EUR 8.50/km², computed), 0.25 km² minimum ([[Sources#^S72|S72]]).

## Cost of one minimum order (ESTIMATE, computed from list prices)
| Order | Calculation | Cost |
|---|---|---|
| Neo archive, SkyWatch | 5 km² × 22.50 | USD 112.50 |
| Neo archive, LAND INFO or Apollo | 25 km² × 22.50 | USD 562.50 |
| Neo tasking, SkyWatch | 5 km² × 32.50 | USD 162.50 |
| Neo tasking at a 100 km² minimum (v1.1 assumption) | 100 km² × 32.50 | USD 3,250 |

The tasking minimum decides whether per-site tasking is affordable: [[Conflicts#^C11]].

## Free and research access
- **ESA Third Party Missions:** non-commercial, non-operational, civil research only. Evaluation normally within 9 weeks, or 4–6 weeks per the FAQ; quota used within a year; archive minimum 25 km², tasking minimum 100 km² ([[Sources#^S73|S73]], [[Sources#^S74|S74]], [[Sources#^S75|S75]], [[Sources#^S76|S76]]). The v1.1 review assumed days: [[Conflicts#^C10]].
- **Earth Engine:** free for non-commercial use only; quota tiers from 2026-04-27; no sustained commercial use without a paid plan ([[Sources#^S77|S77]], [[Sources#^S80|S80]]). A reseller cites USD 500 and 2,000/month plans, possibly dated ([[Sources#^S79|S79]]).
- v1.1 states CDSE openEO gives 10,000 credits a month and Earth Engine 150 EECU-hours a month (course material). The run could not confirm either.

## Not found / not done
- Prices for Planet, KOMPSAT-3A and Vantor (Maxar); the AIM Space offer; CDSE / openEO quotas.
- **T7 archive counts: NOT DONE.** Method in [[w4_archive_counts]]: UP42 catalogue, AOI = park bounding box, count scenes per year and scenes under 20% cloud.

## Data
[[w4_prices]] (20 rows) · [[w4_archive_counts]] (method only). Related: [[Business model v1.1#Data ladder]], [[Tests and gates#T6 Imagery cost]], [[Tests and gates#T7 Archive frequency]], [[Open work#^O7]], [[Open work#^O8]].

## Update 2026-11-07: the team uses Sentinel-2
- Sentinel-2 is the working imagery. VHR prices above matter only for Evidence Packs, MWp by row length, piles and BESS counts. See [[Sentinel-2]].
- The 10,000 openEO credits a month in v1.1 is confirmed as a temporary boost; Sentinel Hub on CDSE adds 10,000 processing units and 10,000 requests a month ([[Sources#^S100|S100]], [[Sources#^S101|S101]]).
