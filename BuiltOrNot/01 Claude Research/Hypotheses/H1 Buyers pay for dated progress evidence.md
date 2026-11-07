---
type: hypothesis
id: H1
desk_status: weakly-supported
interview_status: not-started
segments: ["investor/IPP", law firm, "lenders' technical adviser"]
workstreams: [W3, W5, W6]
source_run: 2026-11-06
tags: [claude-research]
---
> Buyers and their advisers pay for dated progress evidence.

## Interview script (v1.1)
- **Ask:** "In your last Romanian deal with a milestone or COD condition, how did you check progress? Who did it, how long did it take, what did it cost?"
- **Confirms it:** A paid site visit or technical-adviser report, repeated per milestone.
- **Refutes it:** "The seller's EPC report was enough."
- **Follow-up (evidence pack):** "What proof of physical progress do you get between signing and closing, and at what cost?"
- **Who to ask:** investor/IPP, law firm, lenders' technical adviser

## Desk evidence, 6 Nov: Weakly supported
- Kayrros sells construction monitoring to US investors ([[Sources#^S84|S84]]).
- DNV's lender role on Dama Solar includes construction monitoring ([[Sources#^S37|S37]]).
- Romanian deals close at ready-to-build or operating stage, subject to approvals ([[Sources#^S61|S61]], [[Sources#^S63|S63]]).

First targets: DNV and the CMS, Dentons and Nyerges deal teams ([[W3 Reference parks and deals]]).

## Interviews so far
Live list of team interview notes whose `hypotheses` include H1.

```base
filters:
  and:
    - 'type == "interview"'
    - 'hypotheses.contains("H1")'
views:
  - type: table
    name: Interviews on H1
    order:
      - file.name
      - note.owner
      - note.segment
      - note.date
      - note.verdicts
```
