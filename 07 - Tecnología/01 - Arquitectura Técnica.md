# Arquitectura Técnica

## Descripción de la sección

Explica cómo está construido técnicamente el videojuego y cómo se comunican sus componentes.

## Arquitectura

El código está organizado **por feature** (`Assets/_Game/Scripts/<Feature>/`): cada carpeta tiene su código, sus herramientas de editor (`Editor/`) y sus pruebas (`Editor/Tests/`). Las dependencias se conectan con **VContainer** en tres raíces de composición, una por tiempo de vida. Solo `GameFlow` cambia de escena. Las escenas se **generan** con constructores del editor (*OneMind > Build Project*), así que el código es la fuente de verdad. Detalle en `ARCHITECTURE.md` y `AGENTS.md` del repositorio del juego.

```text
Escena Bootstrap ─ GameLifetimeScope (vive toda la aplicación)
│                   SceneLoader, TimeScaleService, SettingsService, GameFlowController
│
├── Escena MainMenu ─ MainMenuLifetimeScope (mientras está el menú)
│                     MainMenuView, MainMenuController, SettingsController
│
└── Escena de nivel ─ GameplayLifetimeScope (una partida: TestingRoom u Outbreak)
                      jugador, ZombieHorde, PlayerPoints, PowerUpController,
                      GameplaySession, HudPresenter, …
```

Flujo de una acción del usuario:

```text
MainMenuView ──evento──► MainMenuController ──► GameFlowController ──► SceneLoader ──► SceneManager de Unity
```

## Componentes principales

| Área | Carpetas | Responsabilidad |
|---|---|---|
| Aplicación y flujo | `ApplicationLifecycle`, `GameFlow`, `Infrastructure` | Arranque, máquina de estados (Menú → Cargando → Jugando ⇄ Pausa → Fin), escenas, ajustes, tiempo. |
| Menús y ajustes | `MainMenu`, `Settings`, `Shared/UI` | Menú principal, selector de niveles y ajustes (UI Toolkit). |
| Jugador | `Player`, `Movement`, `FirstPerson`, `Aiming` | Vida, exotraje, brazos y piernas en primera persona, apuntado y asistencia. |
| Combate y armas | `Combat`, `Weapons`, `RandomWeapons`, `WeaponUpgrades` | Daño, armas, impresora 3D y mejoras. |
| Enemigos y rondas | `Enemies`, `Gameplay` | Horda, rondas, zonas de aparición y sesión de juego. |
| Economía y energía | `Economy`, `PowerUps`, `Batteries`, `Harness`, `Interaction` | Puntos, power-ups, pilas, arnés e interacción con E. |
| Presentación | `Hud`, `Expressions`, `Style`, `Rendering` | HUD, cara de Cuyus, estilo y efectos de render. |
| Niveles | `TestingRoom`, `Outbreak`, `Traps` | Cuarto de pruebas, BROTE (conductos, incinerador, interruptor) y trampas. |

## Comunicación

Los MonoBehaviours leen la entrada y hablan con Unity; las reglas viven en clases de C# simples registradas en el scope (`GameplaySession`, `ZombieHorde`, `PlayerPoints`…). Las vistas exponen eventos de C# (`PlayClicked`, `LevelChosen`…) y nunca deciden qué significan. Los valores de ajuste son ScriptableObjects en `Assets/_Game/Data/`; el estado de la partida vive en objetos de C#, nunca en esos assets. Al descargar una escena se destruye su scope, y recargar el nivel es cómo se reinicia una partida.

## Principios técnicos

- Bajo acoplamiento cuando sea razonable.
- Responsabilidades claras.
- Código mantenible.
- Datos separados de lógica cuando corresponda.
- Evitar dependencias innecesarias.
- Sin `GameManager` global, sin Service Locator y sin singletons por todas partes.

> **Navegación:** [[00 - Índice]] · ← [[04 - Guardado y Configuración]] · [[02 - Motor y Herramientas]] →
