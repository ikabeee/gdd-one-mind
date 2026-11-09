# Datos y Persistencia

## Descripción de la sección

Define qué información necesita conservar el juego y cómo se estructura.

## Datos persistentes

- **Progreso:** no se conserva entre partidas.
- **Configuración:** sensibilidad, campo de visión y volúmenes, guardados en `PlayerPrefs` por `SettingsService`.
- **Inventario:** armas, mejoras y pilas se pierden al reiniciar la partida.
- **Estadísticas:** el resultado se muestra al terminar; no se guardan récords entre sesiones.
- **Desbloqueos:** las puertas vuelven a estar cerradas y la estación experimental bloqueada al iniciar una nueva partida.
- **Otros:** no se han definido otros datos persistentes.

## Modelo de datos

- **Configuración del juego (ScriptableObjects en `Assets/_Game/Data/`):** armas (`WeaponDefinitionSO`), rondas (`RoundSettings`), mutantes (`ZombieSettings` y variantes), puntos (`PointsSettings`), power-ups, pilas, movimiento, estilo, asistencia de apuntado y expresiones de Cuyus.
- **Estado de la partida (objetos de C#, se destruyen con la escena):** vida, puntos, ronda, armas, munición, niveles de mejora, pilas, puertas abiertas, power-ups activos y estilo.
- **Datos del nivel:** `Outbreak_Level.json` (geometría, zonas y marcadores de juego como compras, puertas y puntos de aparición), exportado desde Blender y leído por `OutbreakBuilder`.

## Formato

**Formato de guardado:** `PlayerPrefs` (valores flotantes de 0 a 1 con la clave `settings.<ajuste>`), solo para ajustes.

**Ubicación:** la ubicación estándar de `PlayerPrefs` en Windows (registro del usuario).

**Versionado de datos:** No aplica.

## Migraciones

¿Qué ocurre si cambia la estructura de los datos entre versiones?

No aplica: no se guardan datos de la partida entre sesiones.

> **Navegación:** [[00 - Índice]] · ← [[03 - Requisitos Técnicos]] · [[05 - Seguridad y Riesgos Técnicos]] →
