# Reglas y Estados del Juego

## Descripción de la sección

Define las reglas globales y los estados que puede atravesar el videojuego.

## Estados principales

- **Menú principal:** ofrece Jugar, Controles y Salir.
- **Inicio de partida:** Tannat aparece en la Sala de Contención (Zona 1) con vida completa, 500 puntos y la pistola; las puertas permanecen cerradas. La primera ronda empieza a los 3 s.
- **Combate activo:** los mutantes aparecen en la zona de Tannat y en las zonas abiertas conectadas con ella. El HUD muestra «RONDA N». El jugador puede desplazarse, disparar, recargar y comprar durante la ronda.
- **Transición entre rondas:** cuando no quedan enemigos vivos ni pendientes de aparecer, comienza una pausa de 10 s; el HUD muestra «Siguiente ronda en N». La siguiente ronda aumenta la cantidad, la vida y la velocidad de los mutantes.
- **Pausa:** detiene el juego y permite reanudar, reiniciar o volver al menú.
- **Derrota:** si Tannat cae sin RESPALDO instalado, se desactiva el control y la pantalla «HAS CAIDO» muestra las rondas sobrevividas, las bajas y los puntos. R (o X / botón sur) reintenta y Q (o Select) vuelve al menú. Reintentar reinicia todos los recursos y compras; no se guarda el avance de la partida. Si cae con RESPALDO, se reinicia en 3 s y la partida sigue.

## Transiciones

| Estado origen | Evento | Estado destino | Condición |
|---|---|---|---|
| Menú principal | Elegir "Jugar" | Inicio de partida | — |
| Inicio de partida | Termina la preparación (Zona 1, pistola, 500 puntos; 3 s) | Combate activo | — |
| Combate activo | Muere el último mutante | Transición entre rondas | No quedan enemigos vivos ni pendientes de aparecer |
| Transición entre rondas | Pasan 10 s | Combate activo (ronda + 1) | — |
| Combate activo | Pulsar Esc o M | Pausa | — |
| Pausa | Reanudar | Combate activo | — |
| Pausa | Reiniciar | Inicio de partida | Se pierde el progreso |
| Pausa | Volver al menú | Menú principal | Se pierde el progreso |
| Combate activo | Tannat cae con RESPALDO | Combate activo | Se reinicia en 3 s; se queman RESPALDO y la última pila instalada |
| Combate activo | Tannat cae sin RESPALDO | Derrota | — |
| Derrota | Reintentar (R) | Inicio de partida | Se reinician puntos, armas, mejoras, pilas y puertas |
| Derrota | Volver al menú (Q) | Menú principal | — |

## Reglas globales

1. El progreso de la partida nunca se guarda: al reintentar se vuelve a la ronda 1 con la pistola, 500 puntos, sin mejoras y con las puertas cerradas.
2. No hay ronda final ni condición de victoria; la partida solo termina cuando Tannat cae sin RESPALDO.
3. Los mutantes conocen la posición de Tannat desde que aparecen y solo aparecen en la zona de Tannat y en las zonas abiertas conectadas con ella.
4. La dificultad depende de la ronda, no de la zona: cada ronda aumenta la cantidad, la vida y la velocidad de los mutantes.
5. Toda compra requiere puntos suficientes; si faltan, no se realiza.
6. Tannat solo puede portar dos armas a la vez.

## Casos especiales

Documenta excepciones importantes para evitar interpretaciones diferentes durante la implementación.

- Cambiar de arma durante una recarga la cancela sin añadir munición.
- Comprar un arma con las dos ranuras ocupadas reemplaza el arma activa.
- Si el jugador ya posee el arma de una pared, la misma compra repone su munición por la mitad del precio del arma × (nivel de mejora + 1).
- Si faltan puntos, la compra no se realiza: el costo parpadea en rojo y suena un rechazo.
- Antes de abrir una puerta, el jugador no puede cruzarla y la zona del otro lado no genera mutantes.
- Las bajas con trampa o con PURGA no dan puntos.
- Se puede comprar durante el combate, no solo en la transición entre rondas.

> **Navegación:** [[00 - Índice]] · ← [[06 - Economía y Recursos]] · [[01 - Premisa y Trama]] →
