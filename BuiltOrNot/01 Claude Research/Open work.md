---
type: backlog
status: unassigned
source_run: 2026-11-06
updated: 2026-11-07
tags: [claude-research]
---
Everything still to do, merged from the v1.1 week 1 checklist (7–13 Nov) and the evidence pack's ten gaps. **Nothing here is assigned.** When an item is assigned, the teammate creates a Task note from their own template and puts the item ID (e.g. `O6`) in its `closes` property. Link an item as `[[Open work#^O6]]`.

## Data and registry
- **O1 · Full ATR list with hash.** Download the gov.ro PDF in a browser (robots.txt blocks bots), parse with tabula to CSV, compute sha256. Origin: week 1 + gap 1. Feeds W1, T5. ^O1
- **O2 · ATR locality and plot.** Law 544/2001 request to Transelectrica and the distribution operators. Origin: gap 2. Feeds W1, W2, T5. ^O2
- **O3 · ANRE AI and licence registers.** Download from anre.ro or request under Law 544/2001. Origin: gap 3. Feeds W1. ^O3
- **O4 · The 87.2 GW figure.** Ask ANRE's press office for the monthly ATR series. Origin: gap 4. Resolves [[Conflicts#^C1]]. ^O4
- **O5 · Official CfD lists.** Ministry of Energy page or OPCOM. Origin: gap 5. Resolves [[Conflicts#^C2]], confirms [[Conflicts#^C3]]. ^O5
- **O11 · APM notices.** Crawl apm*.anpm.ro at 1 request/second after a robots.txt check. Origin: gap 10. Feeds W2, T5. ^O11
- **O14 · T5 timed pilot.** Locate 20 ATR holders end to end; record minutes per holder and match confidence (Project record template). Origin: evidence pack T5. Resolves [[Conflicts#^C9]]. ^O14
- **O15 · Data hygiene.** Re-open snippet-only sources (S89, S90, S91, subagent rows); check duplicate CUI 48987667 ([[Conflicts#^C8]]); log and read the two OMV Petrom releases ([[Conflicts#^C6]], [[Conflicts#^C7]]); hash every downloaded file. Origin: evidence pack caveats. ^O15

## Reference parks and imagery
- **O6 · V1 reference set.** Collect developer- or EPC-reported MWp and MWac for 20 parks built 2023–26. Email DRI, OMV Petrom, Engie, Econergy and EDPR first; candidates in [[W3 Reference parks and deals]]. Origin: week 1 + gap 6. Feeds V1. ^O6
- **O7 · T7 archive counts.** A 2-hour UP42 or OneAtlas session: scenes per year and scenes under 20% cloud for the 20 test parks. Do this before building anything that depends on archive dates. Origin: week 1 + gap 7. ^O7
- **O8 · Imagery access.** Request Airbus imagery through ROSPIN / ESA TPM now (weeks, not days: [[Conflicts#^C10]]); ask AIM Space whether KOMPSAT-3A archive covers the test parks; buy one low-minimum archive scene as fallback; ask SkyWatch for a Romanian tasking quote ([[Conflicts#^C11]]). Origin: week 1 + recommendations. ^O8
- **O12 · Screening setup.** Choose 2–3 counties; set up CDSE / openEO and an Earth Engine project, with keys in `.gitignore`. Origin: week 1. Feeds V4. ^O12

## Market
- **O9 · Ten interviews.** 3 investors or advisers, 2 traders, 1 lenders' technical adviser, 2 post-start sellers, 1 module or EPC seller, 1 grid operator. Start with DNV and the CMS, Dentons and Nyerges teams. Ask about past behaviour and spend, not future intent. Origin: week 1 + gap 8. Feeds H1–H8, T8, V6. ^O9
- **O10 · Competitors.** Desk research and demo calls for Lium, i-EM, GEOSAT and Imageryst. Origin: gap 9. Feeds W6. ^O10

## Build
- **O13 · Repo.** Start the repo with a `CLAUDE.md` and the branch-and-PR workflow (Module 4). Origin: week 1. ^O13

## Added 2026-11-07 (Sentinel-2)
- **O16 · Sentinel-2 clear-sky counts.** For the 20 test parks, count clear L2A observations per month for 2023–2026 (Cloud Score+ `cs` ≥ 0.60, or the SCL mask), split by season. This is the Sentinel-2 version of T7, and it decides V2 and winter coverage. See [[Sentinel-2#Working recipe]]. ^O16
- **O17 · TZ-SAM licence.** Ask TransitionZero whether TZ-SAM may be used commercially; until then keep it to research baselines ([[Conflicts#^C17]]). ^O17
- **O18 · V1 decision.** Choose between redefining V1 for Sentinel-2 (footprint × density calibrated by layout, against a single national density) and keeping VHR for MWp. Needs the O6 parks. See [[Sentinel-2#MWp from Sentinel-2]]. ^O18
- **O19 · Accounts.** One free Copernicus Data Space account per teammate (quotas are per user); list who holds which on their Home note. ^O19
