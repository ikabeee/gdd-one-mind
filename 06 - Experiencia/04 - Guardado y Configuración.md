# Guardado y Configuración

## Descripción de la sección

Define cómo se conserva el progreso y qué opciones puede modificar el jugador.

## Guardado

**Tipo:** Sin guardado del progreso de la partida.

**Cuándo se guarda:** Solo se guardan los ajustes, al cambiarlos.

**Qué datos se guardan:** Sensibilidad, campo de visión, volumen general y volumen de música (en `PlayerPrefs`, a través de `SettingsService`). No se guardan récords.

**Cantidad de ranuras:** No aplica.

**Qué ocurre si el guardado falla:** Si no hay un valor guardado, se usa el predeterminado de cada ajuste.

## Configuración

| Categoría | Opciones |
|---|---|
| Audio | Volumen general (0 a 10, predeterminado 8) y música (0 a 10, predeterminado 5). |
| Video | Campo de visión (60 a 110 grados). |
| Controles | Sensibilidad (1 a 10). Esquema fijo, sin reasignación. |
| Accesibilidad | Ver [[03 - Accesibilidad]]. |
| Jugabilidad | Ninguna. |

## Restablecimiento

¿Qué opciones pueden volver a valores predeterminados?

Todas tienen un valor predeterminado; no hay un botón para restablecerlas. *(pendiente)*

> **Navegación:** [[00 - Índice]] · ← [[03 - Accesibilidad]] · [[01 - Arquitectura Técnica]] →
