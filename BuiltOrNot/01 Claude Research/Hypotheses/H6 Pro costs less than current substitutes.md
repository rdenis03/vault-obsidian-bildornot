---
type: hypothesis
id: H6
desk_status: not-found
interview_status: not-started
segments: ["investor/IPP", law firm, "lenders' technical adviser", trader]
workstreams: [W4, W5]
source_run: 2026-11-06
tags: [claude-research]
---
> Pro at €2,000–3,500 a month sits below today's substitute cost.

## Interview script (v1.1)
- **Ask:** "What do you spend a year on market intelligence and site checks for Romania?"
- **Confirms it:** More than €30k a year.
- **Refutes it:** Under €10k a year.
- **Follow-up (evidence pack):** "What is your annual budget for site visits, technical-adviser monitoring and market intelligence on Romania?"
- **Who to ask:** investor/IPP, law firm, lenders' technical adviser, trader

## Desk evidence, 6 Nov: No evidence found
- Substitute spend: NOT FOUND. Only BuiltOrNot's own input costs are known ([[Sources#^S67|S67]], [[Sources#^S79|S79]]).
- Pro costs €24,000–42,000 a year (computed). A €30k substitute spend clears only the lower half of that range, so ask for the actual figure, not a threshold.

Ask about past spend, not future intent: "would you pay €X?" produces polite yeses.

## Interviews so far
Live list of team interview notes whose `hypotheses` include H6.

```base
filters:
  and:
    - 'type == "interview"'
    - 'hypotheses.contains("H6")'
views:
  - type: table
    name: Interviews on H6
    order:
      - file.name
      - note.owner
      - note.segment
      - note.date
      - note.verdicts
```
