---
type: reference
source_run: 2026-11-06
tags: [claude-research]
---
Feasibility tests T1–T11 and the computed results come from [[Business model v1.1]]. "Evidence pack" lines add what the 6 Nov desk run found.

**Feasible for Demo Day. Commercially feasible if three unknowns clear by April 2027:** willingness to pay beyond free data (T8, H6), how often Airbus archive imagery exists over rural Romania (T7), and how long ATR geolocation takes (T5).

## Feasibility tests
### T1 DC capacity from VHR
Technical. Error budget ±5.7% (±3% segmentation, ±1 point of efficiency, ±2° tilt). On 20 simulated parks: MAPE 4.4% (95% CI 2.7–6.2%) against true DC, but 23.8% against AC licences. **Feasible once the reference is DC.** Measure modules as row length × known table depth; a 0.15 m width error moves tilt by 4.2° and area by 3.9%, a 0.30 m error moves area by 8.7%.
Evidence pack: observed DC/AC 1.089–1.425 ([[W8 Technical parameters]]).

### T2 Pile stage
Technical. Shadows are 2–4× longer in Oct–Nov and Feb–Mar than in June; a pile fills 40–50% of a 30 cm pixel. **Conditional: piled area yes, counts unproven.** Order pile-stage imagery for Feb–Mar or Oct–Nov; Dec–Jan has the longest shadows but snow and low cloud.
Evidence pack: piles per MW, pile height and table depth NOT FOUND.

### T3 Site, tables, modules, power blocks
Technical. TZ-SAM detects modules from Sentinel-2; table rows several metres wide resolve at 1.5 m; containers and MV stations at 30–50 cm. **Feasible.**

### T4 Country-wide screening
Technical. 0.1% precision for a single-date bare-soil test; about 43% with stacked filters. **Conditional on the filters.** The substation filter needs the truth table. The false-positive rates are assumptions; V4 replaces them.

### T5 Truth table
Data. The gov.ro list has no coordinates. v1.1: at an assumed 30–45 min per ATR, 1,400 holders take 700–1,050 hours; 30 demo parks take about 20 hours. **Conditional: demo yes, national is a hire.**
Evidence pack: county for every row, CUI for most, zero coordinates ([[Sources#^S2|S2]]); estimate 15–30 min per holder, 350–700 person-hours (ESTIMATE). See [[Conflicts#^C9]] and the pilot in [[Open work#^O14]].

### T6 Imagery cost
Money. Monthly Neo tasking about €2.4M a year; the ladder about €29k. **Not as planned; feasible with the ladder.**

| Scenario | What is bought | Cost per year |
|---|---|---|
| A. v1.0 read literally | Neo tasking at every active site every month (800 site-months at ~€2,990) | ~€2.4M |
| A2. Archive instead of tasking | Neo archive monthly at every active site (~€90 each), if the archive exists | ~€72k |
| B. v1.1 ladder | Sentinel free, SPOT monthly (~€2), Neo archive at 3 key dates per build | ~€29k |

Assumptions: 100 utility builds start a year, each active 8 months on about 0.35 km²; Neo tasking $32.50/km² at a 100 km² minimum; Neo archive €18/km² on UP42 at a 5 km² chargeable minimum; SPOT archive $2.50/km² at 1 km². Sellers differ by up to ×2, so get three quotes.
Evidence pack: a 5 km² tasking minimum at SkyWatch would change scenario A ([[Conflicts#^C11]]).

### T7 Archive frequency
Data. Not public; decides whether 3 key dates per build exist without tasking. **Unknown: query in week 1.**
Evidence pack: NOT DONE; method in [[w4_archive_counts]].

### T8 Market
Money. The 2028 plan needs 20 of about 110 accounts (18%) at €17.5k ACV, which is 9–22% of the €1.6–4.1M pool. **Conditional on interviews.**
Evidence pack: 44 account rows named, spend NOT FOUND ([[W5 Market accounts]]).

### T9 Unit economics, 2028
Money. €350k ARR against about €40k of imagery and cloud gives about 89% gross margin. 4–5 FTE at an assumed €45–60k loaded cost is €180–300k, so roughly break-even. **Conditional on hitting ARR.**

### T10 Legal
Property-insurance and energy uses fall outside AI Act high-risk; ESA TPM is research-only; Earth Engine's free tier is non-commercial; observations-only wording. **Feasible.**

### T11 Team and time
Delivery, 5 weeks to 11 Dec. Earth Engine at 150 EECU-hours a month (5 a day) covers 3 counties; CDSE openEO gives 10,000 credits a month. **Feasible with the triage scope.**
Evidence pack: TPM approval takes weeks, not days ([[Conflicts#^C10]]); openEO and Earth Engine quotas not confirmed.

## Validation tests
Question template (Module 4): in [where, when], does [method] change [metric] compared to [baseline], measured against [reference]?

### V1 DC MWp on 20 parks
Parks built 2023–26. Reference: developer or EPC press MWp, module counts where visible. Baseline: fenced area × typical MWp/ha. Split: leave-one-park-out. **Pass:** MAPE ≤ 8% and better than baseline. **If it fails:** report ranges; sell stage only.
Status: 2 commissioned parks + 4 pipeline projects ([[W3 Reference parks and deals]]).

### V2 Stage dating on 10 parks
Reference: archive image dates bracketing each stage (not press dates, which run weeks off). Baseline: TZ-SAM / GRW first appearance. Split: leave-one-park-out. **Pass:** within one month for stages 1, 4, 5. **If it fails:** sell stage without dates.

### V3 Piled-area fraction on 3 sites
Reference: rows hand-marked on the same native 30 cm image by a second person. Baseline: none (new measure). **Pass:** two people agree within 10 points. **If it fails:** drop the pile stage from packs.

### V4 Screening on 2–3 counties
Reference: hand-checked candidates over 3 months. Baseline: single-date bare-soil test. Split: one held-out county. **Pass:** precision ≥ 30% at recall ≥ 80%. **If it fails:** narrow to ATR-substation zones.

### V5 Truth-table matching on 50 parks
Reference: two independent researchers. Baseline: name match only. **Pass:** ≥ 70% high-confidence links; disagreement ≤ 10%. **If it fails:** narrow to parks ≥ 10 MW.

### V6 Customer pull
Reference: 10 interviews (H1–H8). Baseline: free datasets plus ANRE lists. **Pass:** ≥ 3 pilots, ≥ 1 with a named budget, ≥ 1 lender's adviser interested. **If it fails:** re-segment (ranks 2–4).

## Modelling rules
- Split by site, never by pixel or patch: neighbouring patches share terrain (FireGuard-1 fell from 100% to 50.1% under honest splits).
- Report screening precision at real prevalence, not on a balanced test.
- No probabilities in the product until a reliability diagram on held-out builds is shown.

## Kill criteria
- **Demo Day (2026-12-11):** V1 fails **and** V2 fails → stop the measurement product. Keep the truth table as a data product, or stop.
- **G1, April 2027:** nobody pays for stage, MWp or evidence beyond the free datasets and the gov.ro list → stop the subscription business. Keep Evidence Packs only, or stop.
- **G2, September 2027:** fewer than 3 usable Neo archive dates per build without tasking → re-price packs around tasking, or drop VHR from the tracker.
- **G3, June 2028:** under 70% renewal intent, or no lender's adviser uses a pack in a drawdown → do not expand to new countries.

## Update 2026-11-07: tests with Sentinel-2 as the imagery
- **T7** becomes Sentinel-2 clear-sky counts per month ([[Open work#^O16]]). Neo archive counts matter only if VHR is used.
- **T11:** openEO's 10,000 credits a month is confirmed ([[Sources#^S100|S100]], [[Sources#^S101|S101]]); Earth Engine's 150 EECU-hours is not.
- **V1:** with Sentinel-2 alone, MWp equals area × density, which is the baseline itself, so V1 cannot pass as written ([[Sentinel-2#MWp from Sentinel-2]], [[Open work#^O18]]).
- **V2:** stages 1 and 4 are datable from Sentinel-2; stage 5 is not visible.
- **V3** (piled-area fraction) needs native 30 cm imagery; it cannot run on Sentinel-2.
- **V4:** run it with the Candidate template; verdict counts give precision and recall.
