# Requisitos Técnicos

## Descripción de la sección

Define las condiciones técnicas necesarias para ejecutar y desarrollar el videojuego.

## Requisitos mínimos

**Sistema operativo:** macOS y Windows de 64-bit (objetivos de la build).

**CPU:**

**GPU:**

**RAM:**

**Almacenamiento:** 446 MB (macOS) y 483 MB (Windows) en las builds del 2026-11-12.

**Resolución:** 1920 × 1080 es el objetivo visual, no un requisito mínimo comprobado.

**Conexión:** No se requiere para jugar.

## Requisitos recomendados

**Sistema operativo:**

**CPU:**

**GPU:**

**RAM:**

**Almacenamiento:**

## Objetivos de rendimiento

**FPS objetivo:** 60, pendiente de comprobar en los equipos de prueba. Medición en editor por lotes (peor caso, Rotonda con 32 mutantes): render a GPU de 34.4 ms a 24.5 ms, SetPass de 1 992 a 116 y triángulos de 2.98 M a 2.01 M. Sin medición en player standalone ni en Windows; el dueño reporta problemas tras la ronda 1.

**Tiempo de carga objetivo:**

**Memoria máxima:**

## Restricciones

El alcance actual es un prototipo para PC con teclado y mouse o mando, un nivel (BROTE, con cuatro zonas abiertas y el Incinerador inaccesible; PRUEBAS fuera del menú) y nueve armas obtenibles. Como máximo hay 32 mutantes vivos a la vez; el rendimiento con ese límite debe comprobarse con pruebas.

> [!warning] Recortado para la entrega (2026-11-12)
> Administración, Pruebas Exo, el Cohete y el nivel PRUEBAS en el menú salieron del juego. Ver [[05 - Gestión de Cambios]].

## Compilación

Escenas `Bootstrap`, `MainMenu`, `TestingRoom` y `Outbreak`. Objetivos macOS y Windows de 64-bit, desde el menú *OneMind > Build Player* o en lote con `-executeMethod OneMind.ApplicationLifecycle.Editor.PlayerBuild.FromCommandLine -playerTarget macOS|Windows`, hacia `Builds/macOS/OneMind.app` y `Builds/Windows/OneMind.exe`.


> **Navegación:** [[00 - Índice]] · ← [[02 - Motor y Herramientas]] · [[04 - Datos y Persistencia]] →
