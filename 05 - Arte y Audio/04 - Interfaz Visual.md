# Interfaz Visual

## Descripción de la sección

Documenta la información que el juego muestra al jugador y las reglas visuales de la interfaz.

## HUD

Elementos definidos por la jugabilidad: vida de Tannat, munición, puntos y avisos de interacción. La última imagen compartida por el equipo es la referencia visual del HUD; sus posiciones y medidas quedan pendientes de documentar.

- **Vida:** vida de Tannat.
- **Energía:** no se ha definido una barra; el movimiento no consume estamina.
- **Munición:** munición del arma equipada.
- **Objetivo:** ronda actual; su presentación en el HUD está pendiente de confirmar.
- **Mapa:** no se ha confirmado un minimapa ni una pantalla de mapa.
- **Recursos:** puntos disponibles.
- **Indicadores contextuales:** costo y tecla E al acercarse a una compra.

## Jerarquía visual

¿Qué información debe verse primero, segundo y tercero?

La distribución visual debe seguir la referencia elegida por el equipo. Falta confirmar la ubicación de cada indicador.

Prioridad *(propuesta)*:

1. Vida de Tannat y munición del arma equipada.
2. Puntos disponibles y ronda actual.
3. Indicadores contextuales (costo y tecla E).

## Estados

Al disparar se actualiza la munición. Una compra válida descuenta puntos y reproduce una confirmación. Si faltan puntos, el costo parpadea en rojo y se reproduce un rechazo. Al llegar a cero de vida se muestra la derrota.

## Convenciones

*(propuesta)*

**Tipografía:** Sans serif legible y de estilo técnico, acorde al sistema de Tannat.

**Iconografía:** Iconos simples y planos para vida, munición y puntos.

**Tamaños mínimos:** Texto legible a 1920 × 1080 desde la distancia de juego del showcase.

**Contraste:** Texto claro con contorno o fondo oscuro para leerse sobre cualquier zona del laboratorio.

**Animaciones:** Parpadeo rojo del costo cuando faltan puntos; actualización visible de puntos y munición.

## Pantallas

- **Menú principal:** Jugar, Controles y Salir.
- **Pausa:** reanudar, reiniciar partida o volver al menú.
- **Configuración:** opciones pendientes de acordar.
- **Inventario:** dos ranuras de armas; no se ha definido una pantalla independiente.
- **Mapa:** pantalla no confirmada.
- **Victoria:** no aplica como final del modo endless.
- **Derrota:** muestra las rondas superadas y los puntos totales obtenidos, con posibilidad de reintentar.


> **Navegación:** [[00 - Índice]] · ← [[03 - Entornos]] · [[05 - Audio y Música]] →
