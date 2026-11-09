# Estructura del Contenido

## Descripción de la sección

Organiza el contenido del videojuego en unidades manejables: mundos, capítulos, zonas, niveles, misiones y desafíos.

## Estructura

```text
ONE MIND
├── BROTE — Laboratorio de Neuroplex (mapa principal, rondas sin fin)
│   ├── Sala de Contención (Zona 1, disponible al comenzar)
│   │   ├── Puerta (750) → Administración
│   │   └── Puerta (1,250) → Laboratorio Central
│   ├── Administración ── Puerta (1,000) → Morgue
│   ├── Laboratorio Central ── Puerta (1,000) → Morgue · Puerta (1,000) → Celdas
│   ├── Morgue ── Puerta (1,250) → Pruebas Exo
│   ├── Celdas ── Puerta (1,250) → Pruebas Exo
│   ├── Pruebas Exo (hangar)
│   └── Incinerador (secreto; conductos desde Administración y Pruebas Exo)
└── Cuarto de pruebas (recorrido de entrenamiento con arenas; termina al despejar la última)
```

En BROTE las rondas continúan en las zonas abiertas hasta la derrota; no hay un nivel final.

## Cantidad estimada

| Tipo | Cantidad |
| --- | --- |
| Mundos | El laboratorio de Neuroplex. |
| Niveles | 2: BROTE (6 zonas y el incinerador) y el Cuarto de pruebas. |
| Misiones | Sin misiones; desafío de supervivencia por rondas y la secuencia del incinerador. |
| Enemigos | 1: el científico infectado por Neuroplex (planeado: científico EMZ). |
| Jefes | No hay jefes. |
| NPC | Cuyus como personaje narrativo dentro de Tannat. No hay NPC externos. |
| Objetos | 10 armas, 5 power-ups, 7 pilas, 4 niveles de mejora, 2 trampas y el arnés. |

## Dependencias

¿Qué contenido debe existir antes de otro?

El recorrido comienza en la Sala de Contención. Cada zona se abre pagando una puerta; las zonas lejanas (Morgue, Celdas, Pruebas Exo) requieren haber abierto antes Administración o el Laboratorio Central. Los puntos de aparición de una zona solo se usan cuando está abierta. La mejora experimental requiere la llave del incinerador.

> **Navegación:** [[00 - Índice]] · ← [[04 - Diálogos y Narrativa]] · [[02 - Niveles]] →
