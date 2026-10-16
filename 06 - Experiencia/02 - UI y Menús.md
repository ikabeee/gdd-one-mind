# UI y Menús

## Descripción de la sección

Define la estructura funcional de las interfaces y menús.

## Mapa de navegación

```text
Menú principal
├── Jugar
├── Controles
└── Salir

Durante la partida
└── Pausa
    ├── Reanudar
    ├── Reiniciar
    └── Volver al menú

Después de la derrota
└── Reintentar (comienza una nueva partida)
```

No hay opción de continuar una partida guardada. La configuración adicional queda pendiente.

## Pantallas

### Pantallas de la partida

**Propósito:**  
Iniciar el juego, consultar controles, pausar y conocer el resultado al terminar.

**Elementos:**  
Menú principal, pantalla de controles, HUD, menú de pausa y pantalla de derrota.

**Acciones disponibles:**  
Jugar, consultar controles, salir, reanudar, reiniciar y volver al menú, según la pantalla.

**Estados:**  
Menú, inicio, combate, transición entre rondas, pausa y derrota.

**Transiciones:**  
Jugar inicia en la Zona 1. Pausa permite reanudar o abandonar la sesión. Al reintentar tras la derrota se reinicia el estado de la partida.

## Confirmaciones

Pendiente de decidir si reiniciar o salir al menú requiere confirmación. Ambas acciones interrumpen la partida y deben indicar al jugador qué ocurrirá con su progreso.


> **Navegación:** [[00 - Índice]] · ← [[01 - UX y Flujo del Jugador]] · [[03 - Accesibilidad]] →
