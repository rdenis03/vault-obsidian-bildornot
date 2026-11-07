---
type: guide
updated: 2026-11-07
---
# CLAUDE.md: BuiltOrNot research vault

**BuiltOrNot** is the independent, dated record of what is being built on every approved solar and battery site in Romania: stage, DC MWp, and the paperwork behind it. This Obsidian vault holds the research. `01 Claude Research` is Claude's baseline from 2026-11-06. `02 Team Research` is where seven teammates (TM1–TM7) add to it.

## Map
```
BuiltOrNot/
├── CLAUDE.md                  rules for Claude and for people (this file)
├── Home.md                    human start page
├── 01 Claude Research/        baseline; the team reads it, does not edit it
│   ├── 00 Overview.md         start here: state of W1–W8 and H1–H8, key dates
│   ├── Business model v1.1.md verdict, segments, products, data ladder, triage
│   ├── Sentinel-2.md          the team's imagery: what it shows per stage, free access, recipe
│   ├── Workstreams/           W1–W8, one note each
│   ├── Hypotheses/            H1–H8: interview script, desk status, live interview list
│   ├── Tests and gates.md     T1–T11, V1–V6, kill criteria G1–G3
│   ├── Conflicts.md           C1–C17: figures that disagree, and which to use
│   ├── Open work.md           O1–O19: unassigned backlog
│   ├── Sources.md             S1–S110 and B1–B6, one block ID each
│   └── Data/                  12 CSVs (canonical) + same-name .md table views
└── 02 Team Research/
    ├── 00 Submission/         the Ideathon submission: Submission.md + P01–P12, due 2026-12-11
    ├── Team.md                rules, roster, embedded board
    ├── Team Board.base        live views: roster, tasks, findings, interviews, projects, sources
    └── Teammate 1 … 7/        TM{n} Home.md, the teammate's notes, _templates/
```

## Read order
1. [[00 Overview]].
2. The W or H note that matches the question; [[Sentinel-2]] for anything about imagery.
3. `Data/*.csv` for any number or name.
4. [[Conflicts]] before quoting a figure.
5. Team notes with `status: checked` for anything newer than 2026-11-06.
6. For the submission: [[Submission]], then the P note. Change a part's draft only when asked, and keep P08, P09 and P10 consistent.

## IDs and links
| ID | Meaning | Lives in | Link as |
|---|---|---|---|
| W1–W8 | Workstream | `Workstreams/` | `[[W3 Reference parks and deals]]` |
| H1–H8 | Hypothesis | `Hypotheses/` | `[[H7 Matching ATRs to sites is painful]]` |
| T1–T11 | Feasibility test | Tests and gates | `[[Tests and gates#T5 Truth table]]` |
| V1–V6 | Validation test | Tests and gates | `[[Tests and gates#V1 DC MWp on 20 parks]]` |
| G1–G3 | Stage gate | Tests and gates | `[[Tests and gates#Kill criteria]]` |
| C1–C17 | Conflict | Conflicts | `[[Conflicts#^C9]]` |
| O1–O19 | Open work item | Open work | `[[Open work#^O6]]` |
| S1–S110, B1–B6 | Source | Sources | `[[Sources#^S25\|S25]]` |
| A1–A6 | Run assumption | 00 Overview | none |
| P01–P12 | Submission part | `02 Team Research/00 Submission/` | `[[P02 The problem]]` |
| TM1–TM7 | Teammate | `Teammate {n}/` | `[[TM3 Home]]` |
| TM{n}-TASK/FIND/SRC/INT/PRJ/CAND-### | Team note | owner's folder | by file name |

T is a **test**, TM is a **teammate**. S6, S7, S78 and S92 do not exist.

## Evidence labels
| Label | Meaning |
|---|---|
| NOT FOUND | Searched for and not found. Never means zero. |
| NOT DONE | Step not attempted. |
| ESTIMATE | Assumed or derived, not reported by a source. State the basis. |
| computed | Arithmetic on figures already in the vault. Show the formula. |
| SNIPPET ONLY | Read from a search snippet; re-open the page before use. |
| CONFLICT | Sources disagree; see [[Conflicts]]. |
| FLAG | Data-quality problem inside a source. |
| NOT COMPUTED | sha256 was not taken. |

## Rules
1. **Cite or label every figure:** unit, date of the value, source ID or label.
2. **Never fill a gap with a guess.** Write NOT FOUND or NOT DONE.
3. **Keep the baseline.**
   - Do not rewrite 2026-11-06 text in `01 Claude Research`.
   - Add new facts as a dated `## Update YYYY-MM-DD` section in the note, or as a new conflict, citing the team note they came from.
   - Promote only findings with `status: checked`.
4. **Data.**
   - CSVs are canonical.
   - After editing a CSV, regenerate its `.md` view with the same name.
   - Join on `holder_cui`.
   - In ATR data, `mw_ac` is approved export power (AC), never MWp.
5. **Team folders.**
   - Write in a teammate's folder only for that teammate, using their template and `owner`.
   - Do not assign tasks unless a person asks.
   - Ignore `_templates/`: its YAML holds `{{date}}` placeholders and is not valid until inserted.
6. **Romanian number format:** `91,1 GW` = 91.1 GW; `1.400` = 1,400. Write dates as YYYY-MM-DD and name the currency (EUR, USD, RON).
7. **Quotes** from sources stay under 15 words; paraphrase otherwise.
8. **Imagery is Sentinel-2.**
   - Cite every image by date, product (L2A), tile and clear-sky score (Cloud Score+ `cs` or SCL).
   - Do not claim piles, power blocks or BESS counts from Sentinel-2.
   - MWp from Sentinel-2 is a range ([[Sentinel-2#MWp from Sentinel-2]]).
   - Outputs carry "Contains modified Copernicus Sentinel data [year]".
   - TZ-SAM is non-commercial ([[Conflicts#^C17]]).
9. **Observations, never accusations** about named companies. Public outputs use county aggregates only.

## Common questions
| Question | Where to look |
|---|---|
| What do we know about park X or holder Y? | `Data/w1_registry.csv`, `w3_reference_parks.csv`, `w5_accounts.csv` (search holder and CUI), then team notes with `type: project` |
| Which figure should I use? | [[Conflicts]] |
| Is H3 confirmed? | The H3 note: desk status plus team interviews whose `hypotheses` include H3 |
| What is left to do? | [[Open work]] plus team tasks with `status` not `done` |
| What is each teammate doing? | [[Team Board.base]], or frontmatter of notes under `02 Team Research` |
| What does the business sell, to whom? | [[Business model v1.1]] |
| What is due, and when? | [[Submission]]: 12 parts, 10 minutes, due 2026-12-11 |
| Can we see stage X from space? | [[Sentinel-2#What Sentinel-2 shows, by build stage]] |

## Note schemas
Every note starts with YAML frontmatter. `type` decides the schema. Lists use YAML lists; dates use YYYY-MM-DD.

| type | Properties and allowed values |
|---|---|
| `member` | id `TM{n}` · name · role · university · lead `true`/`false` (one Team Lead) · photo (link to an image) · focus [W ids] · languages [] · status `unassigned`, `active`, `away` |
| `section` | part `P01`–`P12` · title · time · track · status `draft`, `agreed`, `final` · owner (`unassigned` or `TM{n}`) · updated |
| `submission-index` | project_name · team_name · city · track · domain · team_lead · lead_email · github · total_time · intermediate_milestone · submission |
| `task` | owner · status `todo`, `doing`, `blocked`, `done` · priority `high`, `medium`, `low` · closes [O ids] · workstreams [W] · hypotheses [H] · due · created · updated |
| `finding` | owner · status `draft`, `checked`, `promoted` · confidence `high`, `medium`, `low` · workstreams · hypotheses · sources [S ids or team source links] · updates (link to the Claude note it changes) · created |
| `source` | owner · url · title · publisher · language · date_published · date_accessed · source_type `primary`, `primary-mirror`, `secondary`, `tertiary` · access `full`, `snippet-only`, `blocked` · workstreams · sha256 (or NOT COMPUTED) |
| `interview` | owner · date · organisation · role · segment (below) · hypotheses [H] · verdicts [`H1 confirms`, `H1 refutes`, `H1 mixed`, `H1 no-signal`] · spend_eur_year · consent `notes-only`, `recorded`, `anonymous` · status `planned`, `done`, `written-up` |
| `project` | owner · project · holder · holder_cui · technology `PV`, `BESS`, `PV+BESS`, `wind` · mw_ac · mwp_dc · mwh · county · locality · lat · lon · atr_date · paperwork_stage `ATR`, `contract-signing`, `connection-contract`, `AI`, `PIF-planned`, `PIF-done` · build_stage `none`, `1-site`, `2-piles`, `3-tables`, `4-modules`, `5-power-blocks`, `energised`, `unsure` · last_image_date · match_confidence `high`, `medium`, `low` · minutes_spent · sources |
| `candidate` | owner · county · lat · lon · area_ha · tile · last_clear_before · first_clear_after · signal [`bare-soil`, `vegetation-loss`, `pv-signature`, `bright-block`, `sar-change`] · verdict `open`, `pv-start`, `bess-start`, `ploughing`, `harvest`, `greenhouse`, `other-construction`, `no-change` · linked_project |
| `log` | owner · date · searches · pages_opened · files_parsed · rows_collected |
| `workstream`, `hypothesis`, `reference`, `dataset`, `backlog`, `overview` | Claude Research notes; read only |

Interview segments: `investor/IPP`, `law firm`, `lender`, `lenders' technical adviser`, `trader`, `data vendor`, `EPC`, `module or tracker seller`, `O&M`, `insurer`, `BESS integrator`, `grid operator`, `regulator`.

## Glossary
- **ATR** (aviz tehnic de racordare): grid connection approval. Its MW is approved export power, AC.
- **AI** (autorizație de înființare): establishment authorisation from ANRE. In this vault AI never means artificial intelligence.
- **CUI**: Romanian company tax ID; the join key across ATR, CfD and deal records.
- **PIF** (punere în funcțiune): commissioning. **COD**: commercial operation date. **RTB**: ready to build.
- **CfD**: contract-for-difference auction run by the Ministry of Energy.
- **ANRE**: energy regulator. **Transelectrica**: transmission operator. **DSO**: distribution operator.
- **APM**: county environmental protection agency (anpm.ro); its notices may carry plot references. **PUZ**: zonal urban plan.
- **EPC / EPCC**: engineering, procurement, construction (and commissioning) contract. **O&M**: operations and maintenance.
- **LTA**: lenders' technical adviser; certifies drawdowns.
- **MWp**: DC peak capacity of the modules. **MWac**: AC export capacity. **DC/AC**: their ratio (1.09–1.43 observed).
- **BESS**: battery storage. In the ATR list, **IS** = storage and **CEM** = mixed.
- **Build stages (v1.1):** 1 site, 2 piles, 3 tables, 4 modules, 5 power blocks, then energised.
- **Imagery:**
  - Sentinel-2: 10 m optical; satellites 2B and 2C, with 2A extended to end-2027. Sentinel-1: SAR.
  - **L2A**: surface reflectance with **SCL** scene classes. **Cloud Score+** `cs`: per-pixel clear-sky score; ≥ 0.60 counts as clear.
  - **Tile**: Sentinel-2 granule ID (MGRS format, e.g. 34TFR).
  - **NDVI**, **BSI**: vegetation and bare-soil indices, formulas in [[Sentinel-2#Working recipe]].
  - SPOT: 1.5 m.
  - Pléiades Neo: 30 cm native. HD15 is a 15 cm enhanced product, not native.
  - **VHR**: very high resolution.
  - **TPM**: ESA Third Party Missions, research-only access.
  - **CDSE**: Copernicus Data Space Ecosystem.
