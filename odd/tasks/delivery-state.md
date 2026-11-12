---
status: done
---

# Delivery state of the game in the GDD

Objective: the GDD describes the game as it is delivered on 2026-11-13 (the cut version), shows its current art, and records what was cut and why.
Branch: `docs/delivery-state` · Delivery: single-pr · Test runner: none (passive documentation); structural link and embed check.

## Specs

- **S1** "actualizar el GDD junto al arte del juego y lo que tuvimos que recortar": every page agrees with the Unity game at commit `4b01a1dc` of the game repository (facts brief with file evidence, 2026-11-12).
- **S2** "junto al arte del juego": the gallery and the art pages show the current art; the new images are in `assets/`.
- **S3** "lo que tuvimos que recortar": the cuts of the delivery are recorded with their reason in Alcance, Gestión de Cambios and Registro de Decisiones.
- **S4** "en el gdd debe aparecer la version recortada": the body of the GDD describes the cut version; nothing that was cut is described as part of the game.

Assumption: the Google Doc mirror is not updated by this task; it is outward-facing and waits for the owner's word.

## Tasks

| ID | Specs | Route | Status | Evidence |
|---|---|---|---|---|
| T1 | S1–S4 | delegated (read-only explorer: mapping beyond the inline budget) | done | Facts brief of the game, 14 sections, each number with its file |
| T2 | S2 | inline | done | 14 images reviewed one by one and copied into `assets/` (2 replaced, 12 new) |
| T3 | S1, S4 | delegated writer (Muse; parallel units with disjoint files): Visión, Diseño, Contenido, Experiencia | done | 18 pages: four open zones, three doors, nine weapons with their source, fixed printer, HUD and menus as delivered |
| T4 | S1, S2, S4 | delegated writer (Muse): Arte y Audio, Historia y Mundo | done | 10 pages: the 14 new images embedded once each, `## Recortado` in the gallery, audio table with licences |
| T5 | S1, S3, S4 | delegated writer (Muse): Producción, Calidad, Tecnología, Referencia | done | 17 pages: cuts table in Alcance, 18 rows in Gestión de Cambios, 11 decisions, version 0.6.0, BUG-001 to BUG-009 |
| T6 | S1–S4 | inline: review of the three diffs against the brief, link and embed check | done | 0 broken links or embeds; every asset embedded; edit surfaces respected; cut features appear only in cut callouts and record pages; two sentences corrected by the parent |

## Log

- **L1** (2026-11-12) User message: "por mientras mandaras a los agentes de muse a actualizar el GDD junto al arte del juego y lo que tuvimos que recortar. También me harás un artifact sobre cómo funciona el juego, inspiraciones, mecánicas, y modelos 3D". The artifact is a separate page, not part of this repository.
- **L2** (2026-11-12) User message, while the writers ran: "en el gdd debe aparecer la version recortada". Recorded as S4; the handoffs already asked for the delivered game in the body and the cuts only as a record.
- **L3** (2026-11-12) Writers' reports: 45 pages changed, none outside its list; `00 - Índice`, Controles, Pilares de Diseño and Roles untouched. Left as they were because the brief does not settle them: key bindings, acceleration values, CPU/GPU requirements, the menu song's licence, whether dismemberment shows in the build, the weapon renders (they predate the remodel of 2026-11-11 and the gallery says so).
- **L4** (2026-11-12) Review: structural check clean. Parent fixes: an English reason left in the cuts table of Alcance, and the Titanfall entry (it named flight as something Titanfall has). Not done: the level plans still show the level before the cuts (captioned as such); the Google Doc mirror. Risk: none (passive documentation). Next: the owner decides the merge into `main` and the mirror.
