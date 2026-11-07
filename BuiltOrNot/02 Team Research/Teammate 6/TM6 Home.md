---
type: member
id: TM6
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
    - file.inFolder("02 Team Research/Teammate 6")
    - not:
        - file.inFolder("02 Team Research/Teammate 6/_templates")
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
Set once: **Settings → Templates → Template folder location** = `02 Team Research/Teammate 6/_templates`. Then create a note in this folder, name it with the pattern, and run **Templates: Insert template**.

| Template | Use it for | File name |
|---|---|---|
| [[TM6 Task]] | One unit of assigned work | `TM6-TASK-001 Short title` |
| [[TM6 Finding]] | One claim with evidence | `TM6-FIND-001 Short claim` |
| [[TM6 Source]] | One new source you opened | `TM6-SRC-001 Publisher short title` |
| [[TM6 Interview]] | One interview (H1–H8) | `TM6-INT-001 Organisation role` |
| [[TM6 Project record]] | One park or ATR: the truth-table row | `TM6-PRJ-001 Park or holder name` |
| [[TM6 Candidate]] | One Sentinel-2 screening hit to review | `TM6-CAND-001 County place` |
| [[TM6 Log]] | One working session | `TM6-LOG-YYYY-MM-DD` |
