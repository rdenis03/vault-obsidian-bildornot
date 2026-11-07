---
type: submission-index
project_name: BuiltOrNot
team_name:
city:
track:
domain:
team_lead:
lead_email:
github:
total_time: "10 min"
intermediate_milestone: TBC
submission: 2026-12-11
updated: 2026-11-07
---
The Ideathon submission the team is building: 12 parts, P01–P12, delivered in **10 minutes** (about 40 seconds a part) and due on **11 December 2026**. Each part has a note with what it needs, a draft from Claude Research, and what is still open. Nothing is assigned.

## Rules
1. Replace every [bracket] and every "not set" before submission.
2. One number per claim, each with its source.
3. Keep SWOT (P08), PESTEL (P09) and the canvas (P10) consistent with each other.
4. Drafts are drafts: a part becomes `agreed` when the team signs it off, and `final` when it is ready to submit.
5. Front fields (project, team, city) and closing fields (team lead name and e-mail, GitHub link) live in this note's properties.

## Time budget
| Block | Parts | Time |
|---|---|---|
| Team and problem | P01, P02 | 1:30 |
| Research question and solution | P03, P04 | 1:30 |
| Data and method | P05, P06 | 1:30 |
| Existing solutions, SWOT, PESTEL | P07, P08, P09 | 2:30 |
| Business Model Canvas | P10 | 1:30 |
| Work plan and risks | P11, P12 | 1:30 |

P03 applies only to the Scientific Research track; P06 is optional. A Scientific Research team can shorten P10 and give that time to method and results.

## Fixed dates
- Workshops: 12, 19 and 26 Nov; 3 and 10 Dec.
- Intermediate milestone: date to be confirmed by the organisers.
- **Submission: 11 Dec**, with a README and a demo video.

## Status
```base
filters:
  and:
    - 'type == "section"'
views:
  - type: table
    name: Parts
    order:
      - file.name
      - note.time
      - note.track
      - note.status
      - note.owner
```
