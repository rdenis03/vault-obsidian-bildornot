---
type: reference
source_run: 2026-11-06
updated: 2026-11-07
tags: [claude-research]
---
Figures that disagree across sources or between the two Claude outputs. Each item says which value to use until it is resolved. Link one as `[[Conflicts#^C4]]`. "Computed" means arithmetic done on 7 Nov from figures already in the vault.

## Pipeline and auctions
- **C1 · ATR pipeline total.** ^C1
  - Values: more than 80,000 MW across more than 1,400 ATRs on 25 Apr ([[Sources#^S5|S5]]); 91,118 MW across 1,530 projects on 1 Jun ([[Sources#^S22|S22]], [[Sources#^S23|S23]]); more than 78,000 MW issued, per ANRE ([[Sources#^S21|S21]]).
  - 87.2 GW at 1 May: NOT FOUND.
  - Likely cause: scope (selection vs all projects in the connection process).
  - Note: the 1 Jun figure rests on two non-independent secondary sources.
  - **Use:** 91.1 GW for "valid ATRs" (as v1.1 does), with its date.
  - Resolve: [[Open work#^O4]].
- **C2 · Dama Solar CfD strike price.** About EUR 42.2/MWh ([[Sources#^S36|S36]]) vs an ambiguous EUR 45.2 ([[Sources#^S31|S31]]). **Use:** neither in client material until the official list is read. Resolve: [[Open work#^O5]]. ^C2
- **C3 · CfD totals. Likely resolved (computed).** ^C3
  - Values: 4,279 MW ([[Sources#^S34|S34]]); about 4.2 GW plus a 315.8 MW wind round in Dec 2025 ([[Sources#^S35|S35]]); 4.6 GW ([[Sources#^S36|S36]]).
  - R1 (432 + 1,096 MW) plus R2 (1,488 + 1,263 MW) = 4,279 MW, which matches S34 exactly.
  - Adding the 315.8 MW of R3 gives 4,594.8 MW ≈ 4.6 GW, which matches S36.
  - **Use:** 4,279 MW for R1+R2; 4.59 GW including R3.
  - Confirm on the ministry page.

## Parks
- **C4 · Dama Solar DC capacity.** About 1,300 MWp (DNV) ([[Sources#^S37|S37]]) vs almost 1,240 MWp (Profit.ro) ([[Sources#^S36|S36]]); AC 1,044 MW agreed. **Use:** 1,240–1,300 MWp as a range; DC/AC 1.188–1.245. ^C4
- **C5 · Ogrezeni DC capacity.** 761 MWp / 534 MWac (Wikipedia, tertiary) ([[Sources#^S52|S52]]) vs 750 MW DC (snippet) ([[Sources#^S91|S91]]). **Use:** 750–761 MWp; re-open S91 before citing. ^C5
- **C6 · OMV Petrom–CE Oltenia JV COD.** The [[w1_registry]] grant row says 2026 (expected) ([[Sources#^S53|S53]]); OMV Petrom's 2026 release on panel deliveries (about 800,000 panels) says the parks should be operational in 2027. That release has no source ID. **Use:** 2027. The CSV row is left as delivered. ^C6
- **C7 · JV first grant tranche.** About EUR 70M received in Dec 2025 (OMV Petrom 2026 release) vs EUR 16M (OMV Petrom Dec 2025 release). Neither release is in the source log. **Use:** neither until both are logged and read. ^C7
- **C8 · Duplicate CUI in the ATR list.** BESS GURA IALOMIȚEI S.R.L. and Kraftpax SRL both show CUI 48987667 and 352.89 MW ([[Sources#^S2|S2]]). Likely a copy error in the list. **Use:** flag; check the CUI against ONRC or ANAF. ^C8
- **C12 · Two Ișalnița parks (naming trap, not a conflict).** ^C12
  - OMV Petrom's own park: about 89 MWp on the former Doljchim site, EPCC with the Actual Connect consortium ([[Sources#^S55|S55]], [[Sources#^S56|S56]]).
  - The JV's park: about 90 MW on the former CE Ișalnița power-plant site, built by Girisim Elektrik ([[Sources#^S54|S54]]).
  - **Always qualify** which Ișalnița.
- **C13 · Units unclear.** Enel Lumina 63 MW ([[Sources#^S47|S47]]); Rătești 155 MW ([[Sources#^S94|S94]]). **Use:** neither as MWp or MWac until a primary source states the unit. ^C13

## Between the evidence pack and v1.1
- **C9 · T5 matching effort.** Both figures are assumptions, and the unit differs (per ATR vs per holder). ^C9
  - v1.1: 30–45 min per ATR → 700–1,050 hours.
  - Evidence pack: 15–30 min per holder → 350–700 person-hours.
  - **Use:** the range 350–1,050 hours until the 20-holder timed pilot ([[Open work#^O14]]).
- **C10 · ESA TPM approval time.** v1.1 (T11) says approval takes days; ESA says normally within 9 weeks ([[Sources#^S73|S73]]), or 4–6 weeks in its FAQ ([[Sources#^S75|S75]]). ^C10
  - Demo Day is 34 days after 7 Nov, so TPM imagery may not arrive in time.
  - **Use:** weeks. Submit now and buy one low-minimum archive scene as fallback ([[Open work#^O8]]).
- **C11 · Pléiades Neo tasking minimum.** ^C11
  - 100 km²: UP42 ([[Sources#^S69|S69]]), ESA TPM ([[Sources#^S74|S74]]), and the v1.1 T6 assumption.
  - 5 km²: SkyWatch ([[Sources#^S71|S71]]).
  - At USD 32.50/km² (computed): USD 3,250 at 100 km² vs USD 162.50 at 5 km².
  - If SkyWatch's minimum applies to Romanian AOIs, v1.1 weak point 2 ("about €3,000 per new image") and T6 scenario A change by about 20×.
  - Archive minimums also differ: 5 km² (SkyWatch, UP42) vs 25 km² (LAND INFO, Apollo) ([[Sources#^S67|S67]], [[Sources#^S70|S70]], [[Sources#^S71|S71]]).
  - **Use:** v1.1 figures until SkyWatch quotes a Romanian AOI.
- **C15 · v1.1 figures with no source in this vault.** About 3.5 GW of utility-scale solar ever built; 9.1 GW of storage holding building permits; 508 MW "built, awaiting energisation" in July 2026; €1.6–4.1M market size. These come from v1.0 sources [1]–[30], which are not in the vault. **Use:** with care in external material until sourced. ^C15

## Other
- **C14 · Earth Engine paid plans.** USD 500 and 2,000/month from a reseller, possibly dated ([[Sources#^S79|S79]]). **Use:** as indicative only. ^C14

## Added 2026-11-07
- **C16 · Sentinel-2A end date.** The CDSE mission page says three satellites until 2026-03-13 ([[Sources#^S99|S99]]); Sentinel Online announced on 2026-10-09 that the 2A extension continues until 2027-12-31 ([[Sources#^S98|S98]]). **Use:** end of 2027; the CDSE page is out of date. ^C16
- **C17 · TZ-SAM licence vs v1.1 use.** v1.1 names TZ-SAM as a V2 baseline and as commodity panel detection. TZ-SAM is CC BY-NC 4.0 ([[Sources#^S105|S105]], [[Sources#^S106|S106]]); GEM's tracker is CC BY 4.0 ([[Sources#^S38|S38]]). **Use:** TZ-SAM for internal research baselines only, never in paid outputs, unless TransitionZero grants permission ([[Open work#^O17]]). ^C17
