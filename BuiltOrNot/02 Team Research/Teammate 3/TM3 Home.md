---
type: member
id: TM3
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
    - file.inFolder("02 Team Research/Teammate 3")
    - not:
        - file.inFolder("02 Team Research/Teammate 3/_templates")
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
Set once: **Settings → Templates → Template folder location** = `02 Team Research/Teammate 3/_templates`. Then create a note in this folder, name it with the pattern, and run **Templates: Insert template**.

| Template | Use it for | File name |
|---|---|---|
| [[TM3 Task]] | One unit of assigned work | `TM3-TASK-001 Short title` |
| [[TM3 Finding]] | One claim with evidence | `TM3-FIND-001 Short claim` |
| [[TM3 Source]] | One new source you opened | `TM3-SRC-001 Publisher short title` |
| [[TM3 Interview]] | One interview (H1–H8) | `TM3-INT-001 Organisation role` |
| [[TM3 Project record]] | One park or ATR: the truth-table row | `TM3-PRJ-001 Park or holder name` |
| [[TM3 Candidate]] | One Sentinel-2 screening hit to review | `TM3-CAND-001 County place` |
| [[TM3 Log]] | One working session | `TM3-LOG-YYYY-MM-DD` |
