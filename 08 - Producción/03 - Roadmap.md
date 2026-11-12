# Roadmap

## Descripción de la sección

El roadmap organiza el desarrollo en etapas y entregables.

## Etapas

### Concepto

**Objetivo:** Definir la identidad del juego, sus pilares y su alcance.

**Entregables:** GDD versión 0.2.0 o superior, pilares de diseño, alcance inicial y referencias visuales de Tannat y Cuyus.

### Preproducción

**Objetivo:** Validar que el bucle principal funciona.

**Entregables:** Prototipo del MVP en Unity con geometría básica (ver [[01 - Alcance]]), plano de las zonas y primer balance de puntos y costos.

### Producción

**Objetivo:** Construir todos los sistemas y recursos del alcance.

**Entregables:** Las nueve armas obtenibles, IA del científico infectado, rondas, economía, cuatro zonas abiertas, pilas, power-ups, impresora 3D fija, HUD, menús, modelos low poly, animaciones y audio integrados.

### Pruebas

**Objetivo:** Asegurar estabilidad, rendimiento y balance.

**Entregables:** Casos de prueba ejecutados, bugs críticos resueltos, 60 FPS comprobados en equipos de gama media y balance ajustado con playtests.

### Publicación / Entrega

**Objetivo:** Presentar el juego en el showcase de la UT Cancún.

**Entregables:** Versión jugable para macOS y Windows de 64-bit (446 MB y 483 MB) y GDD actualizado.

## Hitos

| Hito | Entregable | Criterio de finalización | Estado |
|---|---|---|---|
| Concepto | GDD con visión, diseño y contenido | Secciones 01 a 07 del GDD completas | Terminado |
| MVP | Bucle jugable en BROTE | Se puede combatir, ganar puntos, comprar, abrir puertas y morir | Terminado |
| Vertical slice | BROTE (cuatro zonas abiertas) con arte integrado | Cumple lo definido en [[01 - Alcance]] | Terminado |
| Beta | Juego con el alcance recortado | Todos los sistemas de la entrega integrados en la build 2026-11-12 | Terminado |
| Entrega | Versión final para el showcase | Cumple los [[04 - Criterios de Aceptación]] | En progreso (builds sin probar en máquina real) |

## Después de la entrega (pendiente)

- Contenido congelado: variantes visuales de los mutantes, rondas especiales, texturas 2, ritmo (pacing), viñetas de Neuroplex, modelos de interactuables restantes y marcadores Intermission.
- Interruptor de energía y puertas con energía.
- Sonido: música dentro de la partida, vidrio, compra, denegación, puertas y rondas; créditos de voces infectadas y disparos.
- Señalización propia del laboratorio.
- Verificación: partida completa en la build, Windows en máquina Windows, costura del menú, pasos, ambiente y murmullo; rendimiento (el dueño reporta problemas tras la ronda 1).
- Tests en rojo: 4 `ZombieVariantBagTests` y `TheDressingStaysWithinSixtyThousandTriangles`; `ShutdownBodyPlayTests` intermitente.


> **Navegación:** [[00 - Índice]] · ← [[02 - Roles y Responsabilidades]] · [[04 - Backlog del Proyecto]] →
