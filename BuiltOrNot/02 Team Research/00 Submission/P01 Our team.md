---
type: section
part: P01
title: "Our team"
time: "30 sec"
track: "both"
status: draft
owner: unassigned
updated: 2026-11-07
---
**Needs:** Name, role and university of each of the seven members, a photo each, the Team Lead marked. The track and the domain (01–12 and its name).
**Rule:** Introduce the team quickly: name and role per person.

## Draft
Read live from each member's Home note (`name`, `role`, `university`, `lead`, `photo`):

```base
filters:
  and:
    - 'type == "member"'
views:
  - type: table
    name: Team
    order:
      - file.name
      - note.name
      - note.role
      - note.university
      - note.lead
      - note.photo
```

- **Track:** not set. Enterprise Software fits the business model, and the canvas (P10) is required for that track. Scientific Research would add [[P03 Research question]].
- **Domain:** not set. The list of domains 01–12 is NOT FOUND in the vault.

## Open
- [ ] Choose the Team Lead: set `lead: true` on one Home note.
- [ ] Confirm the track and the domain; write both in [[Submission]] properties.
- [ ] Add photos: put an image in your own folder and link it in `photo`.

## Evidence
[[Team]]
