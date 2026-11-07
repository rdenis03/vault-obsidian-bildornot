---
type: hypothesis
id: H8
desk_status: contradicted-aggregate-open-project
interview_status: not-started
segments: [trader, "investor/IPP", BESS integrator]
workstreams: [W1, W6]
source_run: 2026-11-06
tags: [claude-research]
---
> Battery build-out matters as much as solar.

## Interview script (v1.1)
- **Ask:** "Do you track storage projects? Which ones and how?"
- **Confirms it:** Yes, with no source.
- **Refutes it:** Not relevant yet.
- **Follow-up (evidence pack):** "Can you see which BESS sites energise next quarter?"
- **Who to ask:** trader, investor/IPP, BESS integrator

## Desk evidence, 6 Nov: Contradicted at aggregate level; open per project
- The run tested a narrower claim: that BESS is tracked as poorly as solar.
- Transelectrica publishes storage connections: 989 MW at 1 Aug; 663 MW connected in 2026 to 20 Aug ([[Sources#^S25|S25]]).
- Press reported 1,094 MW / 2,310 MWh at 1 Sep ([[Sources#^S26|S26]]).
- Kayrros sells a battery storage construction monitor in the US ([[Sources#^S82|S82]]).
- Project-level BESS tracking in Romania: NOT FOUND.

v1.1 tracks batteries from day one ([[Business model v1.1]], change 5).

## Interviews so far
Live list of team interview notes whose `hypotheses` include H8.

```base
filters:
  and:
    - 'type == "interview"'
    - 'hypotheses.contains("H8")'
views:
  - type: table
    name: Interviews on H8
    order:
      - file.name
      - note.owner
      - note.segment
      - note.date
      - note.verdicts
```
