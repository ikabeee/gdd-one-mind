# Datos y Persistencia

## Descripción de la sección

Define qué información necesita conservar el juego y cómo se estructura.

## Datos persistentes

- **Progreso:** no se conserva entre partidas.
- **Configuración:** persistencia pendiente de decidir.
- **Inventario:** las armas compradas se pierden al reiniciar la partida.
- **Estadísticas:** el resultado se muestra al terminar; guardar récords entre sesiones sigue pendiente.
- **Desbloqueos:** la puerta vuelve a estar cerrada al iniciar una nueva partida.
- **Otros:** no se han definido otros datos persistentes.

## Modelo de datos

Durante una partida se necesitan vida, puntos, ronda, armas, munición y estado de la puerta. Esto describe la información del juego; todavía no se ha definido una estructura de archivos ni un modelo de guardado.

## Formato

**Formato de guardado:** No aplica en esta versión. Si se decide guardar récords o configuración, se propone `PlayerPrefs` de Unity.

**Ubicación:** No aplica.

**Versionado de datos:** No aplica.

## Migraciones

¿Qué ocurre si cambia la estructura de los datos entre versiones?

No aplica: no se guardan datos de la partida entre sesiones.

> **Navegación:** [[00 - Índice]] · ← [[03 - Requisitos Técnicos]] · [[05 - Seguridad y Riesgos Técnicos]] →
