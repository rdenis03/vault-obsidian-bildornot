---
type: member
id: TM1
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
    - file.inFolder("02 Team Research/Teammate 1")
    - not:
        - file.inFolder("02 Team Research/Teammate 1/_templates")
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
Set once: **Settings → Templates → Template folder location** = `02 Team Research/Teammate 1/_templates`. Then create a note in this folder, name it with the pattern, and run **Templates: Insert template**.

| Template | Use it for | File name |
|---|---|---|
| [[TM1 Task]] | One unit of assigned work | `TM1-TASK-001 Short title` |
| [[TM1 Finding]] | One claim with evidence | `TM1-FIND-001 Short claim` |
| [[TM1 Source]] | One new source you opened | `TM1-SRC-001 Publisher short title` |
| [[TM1 Interview]] | One interview (H1–H8) | `TM1-INT-001 Organisation role` |
| [[TM1 Project record]] | One park or ATR: the truth-table row | `TM1-PRJ-001 Park or holder name` |
| [[TM1 Candidate]] | One Sentinel-2 screening hit to review | `TM1-CAND-001 County place` |
| [[TM1 Log]] | One working session | `TM1-LOG-YYYY-MM-DD` |
