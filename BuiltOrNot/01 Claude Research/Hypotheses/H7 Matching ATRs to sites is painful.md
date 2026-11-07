---
type: hypothesis
id: H7
desk_status: supported-indirectly
interview_status: not-started
segments: ["investor/IPP", trader, "lenders' technical adviser"]
workstreams: [W1, W2]
source_run: 2026-11-06
tags: [claude-research]
---
> Reconciling ATR, permit and owner records is a real pain.

## Interview script (v1.1)
- **Ask:** "How long did your team spend matching ANRE or gov.ro lists to real sites last quarter?"
- **Confirms it:** Days per quarter.
- **Refutes it:** "We don't need to."
- **Follow-up (evidence pack):** "How long does it take you to locate an ATR holder's site?"
- **Who to ask:** investor/IPP, trader, lenders' technical adviser

## Desk evidence, 6 Nov: Supported indirectly
- The ATR list has no locality, plot or coordinates ([[Sources#^S2|S2]]).
- It is a selection of more than 1,400 ATRs, not the full register ([[Sources#^S5|S5]]).
- Only about 1% of guarantee-posting projects also hold an AI ([[Sources#^S8|S8]]).
- Matching effort is an estimate either way: [[Conflicts#^C9]].

The T5 pilot (time 20 holders) turns this into a measured number ([[Open work#^O14]]).

## Interviews so far
Live list of team interview notes whose `hypotheses` include H7.

```base
filters:
  and:
    - 'type == "interview"'
    - 'hypotheses.contains("H7")'
views:
  - type: table
    name: Interviews on H7
    order:
      - file.name
      - note.owner
      - note.segment
      - note.date
      - note.verdicts
```
