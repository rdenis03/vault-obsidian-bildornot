---
type: hypothesis
id: H4
desk_status: partly-supported
interview_status: not-started
segments: [trader, market analyst, data vendor]
workstreams: [W1, W5, W6]
source_run: 2026-11-06
tags: [claude-research]
---
> Traders want MWp under construction with expected COD by month.

## Interview script (v1.1)
- **Ask:** "What do you use today to forecast new solar? Transelectrica's monthly connections? How far ahead does it see?"
- **Confirms it:** Nothing forward-looking; they build it by hand.
- **Refutes it:** A vendor already sells it.
- **Follow-up (evidence pack):** "What is your error on monthly Romanian PV additions?"
- **Who to ask:** trader, market analyst, data vendor

## Desk evidence, 6 Nov: Partly supported
- Only aggregate outlooks are public ([[Sources#^S24|S24]], [[Sources#^S25|S25]]).
- Kayrros' trader product covers ERCOT and CAISO only ([[Sources#^S81|S81]]).

No trader is named in [[W5 Market accounts]].

## Interviews so far
Live list of team interview notes whose `hypotheses` include H4.

```base
filters:
  and:
    - 'type == "interview"'
    - 'hypotheses.contains("H4")'
views:
  - type: table
    name: Interviews on H4
    order:
      - file.name
      - note.owner
      - note.segment
      - note.date
      - note.verdicts
```
