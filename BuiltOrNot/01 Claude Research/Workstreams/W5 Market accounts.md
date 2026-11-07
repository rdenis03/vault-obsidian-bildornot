---
type: workstream
id: W5
confidence: medium (names), low (spend)
datasets: [w5_accounts]
hypotheses: [H1, H4, H5, H6]
tests: [T8, V6]
source_run: 2026-11-06
tags: [claude-research]
---
**Question.** Who could pay, by name, and what do they spend today?

## Findings
- [[w5_accounts]] has 44 rows: 27 investors or IPPs, 6 law firms, 7 lenders (in 2 rows), 1 lenders' technical adviser, and 10 EPC, O&M or supply-chain firms (in 8 rows).
- DNV is the lenders' technical adviser on Dama Solar, covering technical due diligence, construction monitoring and final acceptance ([[Sources#^S37|S37]]).
- Only Enery and CMS have a contact page recorded.

## Named accounts against the v1.1 segments
| v1.1 rank | Segment | v1.1 estimate | Named here |
|---|---|---|---|
| 1 | Investors, IPP M&A, deal lawyers and advisers | ~40 accounts | 27 investors or IPPs, 6 law firms |
| 2 | Traders, analysts, data vendors | ~15 + 2–3 vendors | **none** |
| 3 | Lenders' technical advisers | ~12 | 1 (DNV) |
| 4 | Post-start sellers: O&M, insurers, BESS integrators | not sized | Simtel Team (EPC and O&M); **no insurers** |
| 5 | Module, tracker and EPC sellers | not sized | 6 EPC or EPCM firms besides Simtel; Longi, Nextracker, Huawei |
| 6 | Transelectrica, DSOs, ANRE | not sized | not listed |

Lenders (7) sit outside the v1.1 ranking because v1.1 reaches them through their technical advisers: EBRD, BSTDB, Exim Banca Românească, NLB, OTP and Intesa on Părău 2 ([[Sources#^S90|S90]]); EIB on the Scatec portfolio ([[Sources#^S51|S51]]).

## Not found
- Spend on site visits, technical-adviser monitoring and market intelligence (T8, H6).
- ANRE trading-licence count; energy data-vendor coverage of Romania.

## Data
[[w5_accounts]] (44 rows). Related: [[Business model v1.1#Who pays, ranked]], [[Tests and gates#T8 Market]], [[Open work#^O9]].
