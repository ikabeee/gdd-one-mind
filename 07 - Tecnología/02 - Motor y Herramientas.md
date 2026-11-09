# Motor y Herramientas

## Descripción de la sección

Documenta las herramientas utilizadas para crear el videojuego y por qué fueron seleccionadas.

## Motor

**Motor:** Unity.

**Versión:** Unity 6 (6000.6.3f1, ver `ProjectSettings/ProjectVersion.txt`).

**Renderizado:** Universal Render Pipeline (URP) 17.6, con postproceso (bloom, viñeta, grano) y shaders propios (`OneMind/PS1Enemy`, `WeaponFX`).

**Física:** Física integrada de Unity; Tannat usa un `CharacterController` y los mutantes navegan con NavMesh (AI Navigation 2.0).

**Sistema de entrada:** Input System 1.20 (`PlayerControls.inputactions`), teclado y mouse, y mando.

## Lenguajes

| Lenguaje | Uso |
| -------- | --- |
| C# | Lógica del juego y herramientas del editor en Unity. |
| Python | Scripts de Blender que construyen modelos, texturas y el nivel BROTE. |
| Bash | `run-tests.sh`, para correr las pruebas sin abrir el editor. |

## Herramientas

| Herramienta | Propósito | Versión |
| ----------- | --------- | ------- |
| Unity Hub y Unity Editor | Motor y editor. | 6000.6.3f1 |
| Blender | Modelado low poly de personajes, armas y del nivel; estudio de ambientación. | 5.x |
| Git y GitHub | Control de versiones y pull requests (`ikabeee/one-mind`). | — |
| Obsidian | Edición de este GDD. | — |

## Dependencias

Lista librerías, paquetes, plugins o servicios externos.

| Paquete | Uso | Versión |
|---|---|---|
| VContainer | Inyección de dependencias (raíces de composición por escena). | 1.19.0 (desde GitHub) |
| Universal RP | Renderizado. | 17.6.0 |
| Input System | Entrada de teclado, mouse y mando. | 1.20.0 |
| AI Navigation | NavMesh de los mutantes. | 2.0.14 |
| Unity Test Framework | Pruebas unitarias y de flujo completo (EditMode). | 1.8.0 |

## Convenciones del proyecto

- **Estructura de carpetas:** por feature en `Assets/_Game/Scripts/<Feature>/`; datos en `Assets/_Game/Data/`; fuentes de Blender en `ArtSource/`.
- **Nomenclatura:** espacios de nombres `OneMind.<Feature>`; nombres que dicen la intención del dominio (sin `Manager`, `Helper` ni `Utils`).
- **Control de versiones:** ramas por feature y pull requests; mensajes con Conventional Commits (`feat(outbreak): …`).
- **Formato de assets:** modelos FBX exportados desde Blender; escenas y HUD generados por código (*OneMind > Build Project*).
- **Convenciones de código:** reglas de arquitectura en `AGENTS.md` (feature primero, composición sobre herencia, inyección explícita).

> **Navegación:** [[00 - Índice]] · ← [[01 - Arquitectura Técnica]] · [[03 - Requisitos Técnicos]] →
