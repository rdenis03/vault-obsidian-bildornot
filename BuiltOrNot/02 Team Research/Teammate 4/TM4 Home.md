---
type: member
id: TM4
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
    - file.inFolder("02 Team Research/Teammate 4")
    - not:
        - file.inFolder("02 Team Research/Teammate 4/_templates")
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
Set once: **Settings → Templates → Template folder location** = `02 Team Research/Teammate 4/_templates`. Then create a note in this folder, name it with the pattern, and run **Templates: Insert template**.

| Template | Use it for | File name |
|---|---|---|
| [[TM4 Task]] | One unit of assigned work | `TM4-TASK-001 Short title` |
| [[TM4 Finding]] | One claim with evidence | `TM4-FIND-001 Short claim` |
| [[TM4 Source]] | One new source you opened | `TM4-SRC-001 Publisher short title` |
| [[TM4 Interview]] | One interview (H1–H8) | `TM4-INT-001 Organisation role` |
| [[TM4 Project record]] | One park or ATR: the truth-table row | `TM4-PRJ-001 Park or holder name` |
| [[TM4 Candidate]] | One Sentinel-2 screening hit to review | `TM4-CAND-001 County place` |
| [[TM4 Log]] | One working session | `TM4-LOG-YYYY-MM-DD` |
