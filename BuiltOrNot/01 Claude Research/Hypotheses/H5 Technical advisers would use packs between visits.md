---
type: hypothesis
id: H5
desk_status: not-tested
interview_status: not-started
segments: ["lenders' technical adviser"]
workstreams: [W5]
source_run: 2026-11-06
tags: [claude-research]
---
> Lenders' technical advisers would use Evidence Packs between site visits.

## Interview script (v1.1)
- **Ask:** "What evidence goes into a drawdown certificate? Would dated imagery count?"
- **Confirms it:** Imagery accepted as supporting evidence.
- **Refutes it:** Only a signed site visit counts.
- **Follow-up (evidence pack):** "Would a dated 30 cm image support a drawdown certificate?"
- **Who to ask:** lenders' technical adviser

## Desk evidence, 6 Nov: Not tested
- DNV is lenders' technical adviser on Dama Solar, with construction monitoring in scope ([[Sources#^S37|S37]]).

Gate G3 depends on this: a lender's adviser must use a pack in a drawdown by June 2028 ([[Tests and gates#Kill criteria]]).

## Interviews so far
Live list of team interview notes whose `hypotheses` include H5.

```base
filters:
  and:
    - 'type == "interview"'
    - 'hypotheses.contains("H5")'
views:
  - type: table
    name: Interviews on H5
    order:
      - file.name
      - note.owner
      - note.segment
      - note.date
      - note.verdicts
```
