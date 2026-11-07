---
type: hypothesis
id: H3
desk_status: mixed
interview_status: not-started
segments: [O&M, insurer, BESS integrator]
workstreams: [W3, W5]
source_run: 2026-11-06
tags: [claude-research]
---
> Post-start sellers want "modules complete" and "built, not energised" signals.

## Interview script (v1.1)
- **Ask** (O&M, insurers, BESS integrators): "When do you pitch a new park, and how do you find out it exists?"
- **Confirms it:** They pitch near completion and find out late.
- **Refutes it:** They already get it from the developer.
- **Follow-up (evidence pack):** "When do you first quote a project?"
- **Who to ask:** O&M, insurer, BESS integrator

## Desk evidence, 6 Nov: Mixed
- O&M is bundled into the EPC at signing: 3 years at Satu Mare 3, 2 years at Ișalnița ([[Sources#^S59|S59]], [[Sources#^S56|S56]]). This weakens H3 for O&M.
- The Ișalnița BESS was contracted during the PV works ([[Sources#^S57|S57]]).
- Insurers: NOT FOUND.

No insurer is named in [[W5 Market accounts]].

## Interviews so far
Live list of team interview notes whose `hypotheses` include H3.

```base
filters:
  and:
    - 'type == "interview"'
    - 'hypotheses.contains("H3")'
views:
  - type: table
    name: Interviews on H3
    order:
      - file.name
      - note.owner
      - note.segment
      - note.date
      - note.verdicts
```
