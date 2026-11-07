---
type: member
id: TM2
name:
role:
university:
lead: false
photo:
focus: []
languages: []
status: unassigned
---
## About
Name, background, what you are best at. Fill in on day one; the [[Team]] roster reads these properties.

Copernicus Data Space account:

## Assigned work
None yet. Work is assigned from [[Open work]]; each item becomes a Task note here.

## My notes
```base
filters:
  and:
    - file.inFolder("02 Team Research/Teammate 2")
    - not:
        - file.inFolder("02 Team Research/Teammate 2/_templates")
    - 'type != "member"'
views:
  - type: table
    name: Open tasks
    filters:
      and:
        - 'type == "task"'
        - 'status != "done"'
    order:
      - file.name
      - note.status
      - note.priority
      - note.due
      - note.closes
  - type: table
    name: All notes
    order:
      - file.name
      - note.type
      - note.status
      - file.mtime
```

## My templates
Set once: **Settings → Templates → Template folder location** = `02 Team Research/Teammate 2/_templates`. Then create a note in this folder, name it with the pattern, and run **Templates: Insert template**.

| Template | Use it for | File name |
|---|---|---|
| [[TM2 Task]] | One unit of assigned work | `TM2-TASK-001 Short title` |
| [[TM2 Finding]] | One claim with evidence | `TM2-FIND-001 Short claim` |
| [[TM2 Source]] | One new source you opened | `TM2-SRC-001 Publisher short title` |
| [[TM2 Interview]] | One interview (H1–H8) | `TM2-INT-001 Organisation role` |
| [[TM2 Project record]] | One park or ATR: the truth-table row | `TM2-PRJ-001 Park or holder name` |
| [[TM2 Candidate]] | One Sentinel-2 screening hit to review | `TM2-CAND-001 County place` |
| [[TM2 Log]] | One working session | `TM2-LOG-YYYY-MM-DD` |
