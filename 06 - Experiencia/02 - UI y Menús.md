# UI y Menús

## Descripción de la sección

Define la estructura funcional de las interfaces y menús.

## Mapa de navegación

```text
Menú principal (UI Toolkit)
├── DISTORSION (modo principal) → pantalla "NIVELES"
│   ├── BROTE
│   └── Cuarto de pruebas
├── Ajustes (sensibilidad, campo de visión, volumen general, música)
└── Salir → "¿Salir de ONE MIND?" (Sí, salir / No)

Durante la partida
└── Pausa (Esc)
    ├── Seguir jugando (clic)
    └── Volver al menú (Q)

Fin de partida (Has caído / Nivel completado)
├── Repetir (R)
└── Volver al menú (Q)
```

No hay opción de continuar una partida guardada.

## Pantallas

### Pantallas de la partida

**Propósito:**  
Elegir nivel, ajustar opciones, pausar y conocer el resultado al terminar.

**Elementos:**  
Menú principal con selector de niveles (cada nivel tiene una tarjeta con su descripción), ajustes, HUD, pausa y pantalla de fin de partida.

**Acciones disponibles:**  
Elegir nivel, cambiar ajustes, salir, seguir jugando, repetir y volver al menú, según la pantalla. Todo se puede usar con teclado y mouse o con mando.

**Estados:**  
Menú, cargando, jugando, pausa y fin de partida.

**Transiciones:**  
Elegir un nivel lo carga. La pausa congela el juego. Repetir vuelve a cargar el nivel desde cero.

## Confirmaciones

Salir del juego pide confirmación ("SE CERRARA EL JUEGO"). Volver al menú desde la pausa no pide confirmación.

> **Navegación:** [[00 - Índice]] · ← [[01 - UX y Flujo del Jugador]] · [[03 - Accesibilidad]] →
