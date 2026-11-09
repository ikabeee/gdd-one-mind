---
status: pending
---

# Mirror the repository GDD into the Google Doc

Objective: copy every GDD update made in this repository into the team's Google Doc "GDD-Villafaña".
Branch: none (external document) · Delivery: in-place edits to the same Google Doc · Test runner: none; read the Doc back after each edit.

## Specs

- **S1** "https://docs.google.com/document/d/1_9RelGTAb7sqcRxjx2zxVED2G2YciGNbW05Vnx77EvA/edit?tab=t.0#heading=h.wwqycsrj3010 lo que vayas actualizando del gdd dentro del repositorio lo metes aqui en este docs"

## Tasks

| ID | Specs | Route | Status | Evidence |
|---|---|---|---|---|
| T1 | S1 | inline | blocked | The connected Google account cannot edit the Doc: Drive metadata reports `canEdit: false` (owner: the project lead) |
| T2 | S1 | inline | pending | Images: the Docs API only inserts images from a public URL; the GitHub repo is public, so pushed `assets/` could be embedded through raw GitHub URLs (needs the user's approval to push) |

## Log

- **L1** (2026-11-09) User request quoted in S1.
- **L2** (2026-11-09) Drive metadata: title "GDD-Villafaña", Doc still at GDD version 0.2.0; `capabilities.canEdit: false` for the connected account.
