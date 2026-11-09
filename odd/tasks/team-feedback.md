---
status: done
---

# Team feedback alignment with the Unity game

Objective: resolve the team's GDD feedback, using the implemented Unity game as the source of truth; anything Unity does not settle is a team decision.
Branch: `docs/gdd-unity-alignment` · Delivery: ask-on-risk · Test runner: none (passive documentation); structural link check.

## Specs

Team feedback, verbatim ("Cosas a corregir/agregar"):

- **S1** "Esta establecido que solo hay 2 zonas"
- **S2** "El movimento de tannat, esta limitado a WASD, y salto simple"
- **S3** "Solo se toma en cuenta las armas pistola, escopeta y smg"
- **S4** "Hay que establecer que mejoras se van a poder usar. (Actualmente esta “Compra o recogida de drops, según el modelo elegido”)"
- **S5** "Validar si lo de ”Diálogos y narrativa”, se va. a mantener, o que se hara"
- **S6** "Determinar que tarifa se manejara para los refill de municiones"
- **S7** "”Falta definir la distribución de obstáculos del escenario.” en 02 - Niveles Descripción de la sección"
- **S8** "Falta definir daño y velocidad de los mutantes, y la velocidad de tannat"
- S9 and S10 (art) are covered by [art-gallery](art-gallery.md) S2.

Assumption: where the Unity game already implements an answer, the GDD documents it; S5 is a team decision.

## Tasks

| ID | Specs | Route | Status | Evidence |
|---|---|---|---|---|
| T1 | S1–S8 | delegated (read-only explorer: mapping beyond the inline budget) | done | Unity facts with file evidence: movement and input, health, enemy tuning, upgrades, BROTE layout, narrative, levels, points |
| T2 | S1, S7 | delegated writer (context backstop) | done | Niveles: zone, door, trap and spawn tables replace «Falta definir la distribución de obstáculos»; Estructura del Contenido tree; PRUEBAS level |
| T3 | S2, S8 | delegated writer (context backstop) | done | Controles (keyboard + gamepad), Mecánicas (movement table, Tannat health), Enemigos y NPC (damage, speed, health, attacks) |
| T4 | S3, S4, S6 | delegated writer (context backstop) | done | Objetos (10-weapon table, real Mejoras list), Economía (points, style rank, ammo refill price rule) |
| T5 | S5 | delegated writer: document what the game has, plus a team-decision callout | done | Diálogos y Narrativa documents the game's environmental narrative and Cuyus's reactions, with a «Decisión del equipo» callout |

## Log

- **L1** (2026-11-09) User message: "TAMBIEN TENGO INFORMACION DE FEEDBACK DE MI EQUIPO", followed by the list quoted in S1–S8 and the two art items.
- **L2** (2026-11-09) Unity facts: BROTE has 6 zones plus the secret Incinerador basement (menu: "6 ZONAS") and a second level, PRUEBAS (sandbox); 10 weapons; ammo refill = half the gun price × (upgrade tier + 1); MK1–MK4 upgrade stations, 3D printer 950, Exo harness 1500; Tannat runs 13 m/s with double jump, slide, dash and stomp; scientist hits for 40, walks 4 m/s (+0.3/round, cap 9); no dialogue in game.
- **L3** (2026-11-09) Decision: S5 is the team's call, so the writer documents what the game has and adds a team-decision callout instead of deleting the section. Writer delegated by the context backstop; the parent owns git and the art notes.
- **L4** (2026-11-09) Writer report: 32 notes updated, S1–S8 covered; GDD version 0.5.0. Link check clean except the README's literal `[[Wikilinks]]` example (pre-existing). Remaining «SMG / dos zonas» hits are history rows, the glossary («conecta dos zonas») and the spec quotes. Parent fixed the stale line in Referencias e Inspiración, removed the resolved «Por alinear» callouts in the art notes and added Registro rows for gamepad, movement and visual style. Writer assumptions: refill multiplier ×1 unupgraded … ×5 at MK4 (from the formula); the Cohete refills only through an MK upgrade or the MUNICIÓN power-up; gamepad bindings for interact and aim left empty (not in the facts).
- **L5** (2026-11-09) User: "Mergea a main directo cuando el agente del feedback termine". Closed; merged into main. Risk: none (passive documentation). Next: [google-doc-mirror](google-doc-mirror.md).
