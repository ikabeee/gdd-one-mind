# Reglas y Estados del Juego

## Descripción de la sección

Define las reglas globales y los estados que puede atravesar el videojuego.

## Estados principales

- **Menú principal:** ofrece Jugar, Controles y Salir.
- **Inicio de partida:** Tannat aparece en la Zona 1 con vida completa, cero puntos y la pistola; la puerta permanece cerrada.
- **Combate activo:** los mutantes aparecen en las zonas habilitadas. El jugador puede desplazarse, disparar, recargar y comprar durante la ronda.
- **Transición entre rondas:** cuando no quedan enemigos vivos ni pendientes de aparecer, comienza una pausa de entre 3 y 5 segundos, como valor inicial de prueba. La siguiente ronda aumenta la cantidad y la vida de los mutantes.
- **Pausa:** detiene el juego y permite reanudar, reiniciar o volver al menú.
- **Derrota:** al llegar a cero de vida, se desactiva el control y se muestran las rondas superadas y los puntos totales obtenidos. Reintentar reinicia todos los recursos y compras; no se guarda el avance de la partida.

## Transiciones

| Estado origen            | Evento                                              | Estado destino             | Condición                                         |
| ------------------------ | --------------------------------------------------- | -------------------------- | -------------------------------------------------- |
| Menú principal          | Elegir "Jugar"                                      | Inicio de partida          | —                                                 |
| Inicio de partida        | Termina la preparación (Zona 1, pistola, 0 puntos) | Combate activo             | —                                                 |
| Combate activo           | Muere el último mutante                            | Transición entre rondas   | No quedan enemigos vivos ni pendientes de aparecer |
| Transición entre rondas | Pasan 3-5 s                                        | Combate activo (ronda + 1) | —                                                 |
| Combate activo           | Pulsar Esc o M                                      | Pausa                      | —                                                 |
| Pausa                    | Reanudar                                            | Combate activo             | —                                                 |
| Pausa                    | Reiniciar                                           | Inicio de partida          | Se pierde el progreso                              |
| Pausa                    | Volver al menú                                     | Menú principal            | Se pierde el progreso                              |
| Combate activo           | La vida de Tannat llega a 0                         | Derrota                    | —                                                 |
| Derrota                  | Reintentar                                          | Inicio de partida          | Se reinician puntos, armas, mejoras y la puerta    |

## Reglas globales

1. El progreso de la partida nunca se guarda: al reintentar se vuelve a la ronda 1 con la pistola, sin puntos ni mejoras y con la Zona 2 cerrada.
2. No hay ronda final ni condición de victoria; la partida solo termina cuando la vida de Tannat llega a cero.
3. Los mutantes conocen la posición de Tannat desde que aparecen y solo aparecen en zonas habilitadas.
4. La dificultad depende de la ronda, no de la zona: cada ronda aumenta la cantidad y la vida de los mutantes.
5. Toda compra requiere puntos suficientes; si faltan, no se realiza.
6. Tannat solo puede portar dos armas a la vez.

## Casos especiales

Documenta excepciones importantes para evitar interpretaciones diferentes durante la implementación.

- Cambiar de arma durante una recarga la cancela sin añadir munición.
- Comprar un arma con las dos ranuras ocupadas reemplaza el arma activa.
- Si el jugador ya posee el arma de un soporte, puede comprar su munición por un costo menor.
- Si faltan puntos, la compra no se realiza: el costo parpadea en rojo y suena un rechazo.
- Antes de abrir la puerta, ni el jugador puede cruzar ni los mutantes pueden aparecer en la Zona 2.
- Se puede comprar durante el combate, no solo en la transición entre rondas.

> **Navegación:** [[00 - Índice]] · ← [[06 - Economía y Recursos]] · [[01 - Premisa y Trama]] →
