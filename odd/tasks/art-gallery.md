---
status: done
---

# Art gallery in the GDD

Objective: place the game's existing art (sketches, characters, enemy, weapons, level, UI) in the GDD, based on the Unity project.
Branch: `docs/gdd-unity-alignment` · Delivery: single slice (images are binary; authored Markdown is small) · Test runner: none (passive documentation); structural check that every wikilink and embed resolves.

## Specs

- **S1** "falta colocar en el gdd el arte del juego, bocetos, armas, personajes, zombies, etc" — "Con base a lo que tenemos del proyecto de one mind (unity)".
  - Images come from the Unity project and its art exports: `~/Documents/one-mind/OneMind_Assets/Renders`, `characters_v2`, `trailer/storyboard/panels`, `outbreak/`.
  - Copied into `assets/{characters,enemies,weapons,environment,ui,storyboard}`, resized and palette-quantized to keep the repo light; file names unique in the vault so `![[name]]` embeds resolve.
- **S2** Team feedback items about art (verbatim from the team list):
  - "En “05 — Arte y Audio”, falta Iluminación: Materiales: Paleta de color Colores principales: Colores secundarios: Colores para información jugable: Referencias"
  - "En “02 - Personajes y Animación”, falta definir Animaciones"

Assumption: the enemy shown is the Neuroplex infected scientist, the only enemy in the Unity levels; the retired "Tanguy" enemies appear only as a discarded design.

## Tasks

| ID | Specs | Route | Status | Evidence |
|---|---|---|---|---|
| T1 | S1 | inline | done | 75 images in `assets/`; the scientist had no render, so it was rendered headless from `Enemy_Scientist.blend` (not saved) |
| T2 | S1 | inline | done | New note `05 - Arte y Audio/06 - Galería de Arte.md`; index and navigation updated |
| T3 | S1, S2 | inline | done | Dirección de Arte, Personajes y Animación, Entornos, Interfaz Visual and Personajes updated from the Unity project; version 0.4.0 |
| T4 | S1 | inline | done | Structural check: no duplicate file names; every new embed and link resolves (only pre-existing `00 - Índice` NFD/NFC mismatches remain) |

## Log

- **L1** (2026-11-09) User request: "Con base a lo que tenemos del proyecto de one mind (unity) falta colocar en el gdd el arte del juego, bocetos, armas, personajes, zombies, etc"
- **L2** (2026-11-09) Findings: Unity has 10 weapons, 7 BROTE zones and one enemy (scientist); GDD design notes still describe pistol/SMG/shotgun and 2 zones. Flagged in the gallery as "Por alinear"; fixing them belongs to [team-feedback](team-feedback.md).
- **L3** (2026-11-09) User added the team feedback; its two art items (S2) were covered here.
- **L4** (2026-11-09) Closed. Commit 49194cd on `docs/gdd-unity-alignment` (not pushed). Review assess (committed range vs `main`, untracked excluded): medium, `review_due: false` (`under_budget`). Risk: none (passive documentation). Pending: the Google Doc copy of these changes ([google-doc-mirror](google-doc-mirror.md)). Next: [team-feedback](team-feedback.md).
- **L5** (2026-11-09) Correction: BROTE has six zones plus the secret Incinerador basement, not seven zones (commit 1c88f82).
