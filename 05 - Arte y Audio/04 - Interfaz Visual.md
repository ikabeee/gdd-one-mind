# Interfaz Visual

## Descripción de la sección

Documenta la información que el juego muestra al jugador y las reglas visuales de la interfaz.

## HUD

El HUD es de píxel, con una ligera perspectiva y balanceo que siguen a la cámara.

- **Vida:** vida de Tannat (100, o 160 con BLINDAJE).
- **Energía:** no hay estamina; los íconos de DASH y STOMP muestran si están disponibles.
- **Munición:** cargador y reserva del arma en la mano, ícono del arma y avisos "RECARGANDO" y "SIN MUNICION".
- **Objetivo:** ronda actual, anunciada con un glitch al empezar ("RONDA N"), y mutantes restantes.
- **Mapa:** no hay minimapa.
- **Recursos:** puntos disponibles.
- **Pilas:** la bahía de pilas de Tannat, con color e ícono de cada pila instalada.
- **Estilo:** rango (D a S), barra del rango, multiplicador ("ESTILO x2") y avisos de lo que lo subió ("HEADSHOT", "AEREA", "CADENA x3", "COMBO x5").
- **Power-ups activos:** nombre y tiempo restante (PUNTOS DOBLES, LETAL, IMPULSO).
- **Cuyus:** retrato con la cara que reacciona a la partida ("NINA A BORDO").
- **Indicadores contextuales:** tecla E, acción y costo al acercarse a una compra; mira central que desaparece al apuntar.

## Jerarquía visual

¿Qué información debe verse primero, segundo y tercero?

1. Vida de Tannat y munición del arma en la mano.
2. Puntos, ronda y disponibilidad de dash y stomp.
3. Estilo, pilas, power-ups e indicadores contextuales.

## Estados

Al disparar se actualiza la munición. Una compra válida descuenta puntos. Si faltan puntos aparece "Puntos insuficientes". Al recibir daño, el HUD hace glitch. Con RESPALDO se muestra "RESPALDO reiniciando...". Al caer aparece "HAS CAIDO" con el progreso, las bajas y los puntos.

## Convenciones

**Tipografía:** fuente de píxel; los textos van sin acentos porque la fuente no los dibuja.

**Iconografía:** íconos de píxel (dash y stomp de 9 px, armas de 16×7 px, pilas de 7×7 px).

**Tamaños mínimos:** texto legible a 1920 × 1080 desde la distancia de juego del showcase (pendiente de comprobar en sitio).

**Contraste:** texto con sombra para leerse sobre cualquier zona; las pilas se distinguen por ícono además de por color.

**Animaciones:** glitch de ronda y de daño, cuadros de impacto, efecto de dash y balanceo del HUD.

## Pantallas

- **Menú principal:** Niveles (BROTE y Cuarto de pruebas), Ajustes y Salir (con confirmación).
- **Pausa:** "PAUSA"; clic para seguir jugando, Q para volver al menú.
- **Configuración:** sensibilidad, campo de visión, volumen general y música.
- **Inventario:** dos ranuras de armas en el HUD; sin pantalla aparte.
- **Mapa:** no hay.
- **Victoria:** solo en el Cuarto de pruebas ("NIVEL COMPLETADO", con tiempo, bajas, puntos y mejor estilo).
- **Derrota:** "HAS CAIDO" con el progreso, las bajas y los puntos; R para repetir, Q para volver al menú.

> **Navegación:** [[00 - Índice]] · ← [[03 - Entornos]] · [[05 - Audio y Música]] →
