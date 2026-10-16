# Motor y Herramientas

## Descripción de la sección

Documenta las herramientas utilizadas para crear el videojuego y por qué fueron seleccionadas.

## Motor

**Motor:** Unity.

**Versión:** Unity 6.6

**Renderizado:** Universal Render Pipeline (URP), adecuado para low poly y equipos de gama media.

**Física:** Física integrada de Unity; Character Controller para Tannat y raycasts para el disparo.

**Sistema de entrada:** Input System de Unity.

## Lenguajes

| Lenguaje | Uso                                             |
| -------- | ----------------------------------------------- |
| C#       | Programación de la lógica del juego en Unity. |

## Herramientas

| Herramienta | Propósito                                             | Versión                |
| ----------- | ------------------------------------------------------ | ----------------------- |
| Blender     | Modelado 3D low poly de personajes, armas y escenario. | Pendiente de confirmar. |
| Git         | Control de versiones.                                  |                         |
| Obsidian    | Documentación del GDD.                                |                         |

## Dependencias

Lista librerías, paquetes, plugins o servicios externos.

- **AI Navigation (NavMesh):** rutas de persecución de los mutantes.
- **TextMeshPro:** textos del HUD y los menús.
- **Input System:** entrada de teclado y mouse.

## Convenciones del proyecto

*(propuesta)*

- **Estructura de carpetas:** `Assets/_Project/` con `Scripts`, `Prefabs`, `Models`, `Materials`, `Audio`, `UI` y `Scenes`.
- **Nomenclatura:** archivos en inglés; PascalCase para scripts y prefabs (`WeaponController`, `Mutant`).
- **Control de versiones:** Git con `.gitignore` de Unity y Git LFS para modelos, texturas y audio.
- **Formato de assets:** modelos `.fbx` exportados desde Blender, texturas `.png`, audio `.wav` u `.ogg`.
- **Convenciones de código:** convenciones estándar de C#; una responsabilidad por script.

> **Navegación:** [[00 - Índice]] · ← [[01 - Arquitectura Técnica]] · [[03 - Requisitos Técnicos]] →
