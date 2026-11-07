---
type: candidate
owner: TM2
county:
lat:
lon:
area_ha:
tile:
last_clear_before:
first_clear_after:
signal: []
verdict: open
linked_project:
created: {{date:YYYY-MM-DD}}
---
> [!info] One change flagged by Sentinel-2 screening. Decide what it is before it becomes a Project record. Verdict counts give V4's precision.

## Change
| Date | Product | Clear-sky (cs or SCL) | NDVI | BSI | Note |
|---|---|---|---|---|---|
|  | S2 L2A |  |  |  | before |
|  | S2 L2A |  |  |  | after |

## Look-alike check
- [ ] Persists over 2 or more clear passes (ploughing and harvest do not)
- [ ] Not a greenhouse, plastic mulch, quarry or car park
- [ ] Linear roads or fences visible
- [ ] Near an ATR holder's county or a substation
- [ ] Sentinel-1 shows change too (cloudy weeks)

## Verdict
What it is, and why. If `pv-start` or `bess-start`, create a Project record and link it in `linked_project`.
