---
type: team-index
updated: 2026-11-07
---
Seven research workspaces, TM1–TM7, plus the shared [[Submission]] (P01–P12, due 11 Dec). **No work is assigned yet.** The backlog is [[Open work]]; the research baseline is [[00 Overview]].

## Teammates
[[TM1 Home]] · [[TM2 Home]] · [[TM3 Home]] · [[TM4 Home]] · [[TM5 Home]] · [[TM6 Home]] · [[TM7 Home]]

Each folder holds a Home note and `_templates/` with seven templates: Task, Finding, Source, Interview, Project record, Candidate, Log. Names, roles and focus go in each Home note's properties; the Roster view below reads them.

## Rules
1. Write only in your own folder; `00 Submission` is shared, and a part's `owner` edits it. Claude Research is the baseline: do not edit it. Disagree in a Finding with `updates` set to the note you challenge.
2. Name files `TM{n}-{TYPE}-{###} Short title`. Types: TASK, FIND, SRC, INT, PRJ, CAND. Logs: `TM{n}-LOG-YYYY-MM-DD`.
3. Every number gets a unit, a date and a source. Cite Claude sources as `[[Sources#^S25|S25]]`, team sources by their note.
4. Use the labels NOT FOUND, NOT DONE, ESTIMATE, SNIPPET ONLY and CONFLICT. Never fill a gap with a guess.
5. A Finding is `checked` once a second teammate has re-read its sources. Only checked findings are promoted into Claude Research.
6. Imagery is Sentinel-2 ([[Sentinel-2]]). Every image cited gets date, product, tile and clear-sky score; outputs carry "Contains modified Copernicus Sentinel data [year]".
7. Interviews: ask about past behaviour and spend, not future intent. Hypotheses go in `hypotheses`, results in `verdicts` (e.g. `H1 confirms`).

Field values for every template are listed in [[CLAUDE#Note schemas]].

## Templates setup (once per person)
1. Settings → Core plugins → turn on **Templates** and **Bases**.
2. Settings → Templates → Template folder location → your own `02 Team Research/Teammate {n}/_templates`.
3. New note in your folder → name it with the pattern → command **Templates: Insert template**.

If the vault is shared through git, the template-folder setting stays personal: `.obsidian/templates.json` is in `.gitignore`.

## Board
![[Team Board.base]]
