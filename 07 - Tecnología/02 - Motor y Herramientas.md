# Motor y Herramientas

## Descripción de la sección

Documenta las herramientas utilizadas para crear el videojuego y por qué fueron seleccionadas.

## Motor

**Motor:** Unity.

**Versión:** Unity 6000.6.3f1.

**Renderizado:** Universal Render Pipeline 17.6.0; renderers PC, Mobile y Viewmodel; espacio de color lineal.

**Navegación:** AI Navigation 2.0.14; el NavMesh se hornea al cargar desde los colliders de física.

**Sistema de entrada:** Input System 1.20.0 (teclado, mouse y mando).

## Lenguajes

| Lenguaje | Uso                                             |
| -------- | ----------------------------------------------- |
| C#       | Programación de la lógica del juego en Unity. |

## Herramientas

| Herramienta | Propósito                                             | Versión                |
| ----------- | ------------------------------------------------------ | ----------------------- |
| Blender 5.2 | Modelado 3D low poly de personajes, armas y escenario, con scripts Python de construcción. | 5.2 |

## Dependencias

- VContainer 1.19.0 (inyección de dependencias).
- UI Toolkit (menú principal, pausa, ajustes y game over); prefab uGUI con TextMeshPro (HUD); overlay IMGUI (prompts).
- Unity Test Framework 1.8.0, EditMode (unitarias y de flujo completo); se corren con `./run-tests.sh [filtro]`.

## Convenciones del proyecto

- Código organizado por funcionalidad (`Scripts/<Función>`), sin `.asmdef` bajo `Assets/_Game`.
- Raíces de composición (`GameLifetimeScope` y un scope por escena) con inyección por constructor; sin GameManager ni service locator.
- Las vistas reportan intención y los controladores deciden; transiciones en `GameFlowController`, cargas en `SceneLoader`.
- ScriptableObjects para configuración, clases C# para estado y MonoBehaviours como adaptadores finos.
- Escenas, HUD y nivel generados por builders de editor, no editados a mano.

> **Navegación:** [[00 - Índice]] · ← [[01 - Arquitectura Técnica]] · [[03 - Requisitos Técnicos]] →
