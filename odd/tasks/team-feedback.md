---
status: pending
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
| T1 | S1–S8 | delegated (read-only explorer: mapping beyond the inline budget) | in-progress | |
| T2 | S1, S7 | inline | pending | |
| T3 | S2, S8 | inline | pending | |
| T4 | S3, S4, S6 | inline | pending | |
| T5 | S5 | ask | pending | |

## Log

- **L1** (2026-11-09) User message: "TAMBIEN TENGO INFORMACION DE FEEDBACK DE MI EQUIPO", followed by the list quoted in S1–S8 and the two art items.
