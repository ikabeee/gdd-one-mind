# Reglas y Estados del Juego

## Descripción de la sección

Define las reglas globales y los estados que puede atravesar el videojuego.

## Estados principales

El flujo de la aplicación es una máquina de estados (`GameFlowController`): Menú principal → Cargando → Jugando ⇄ Pausa, y Jugando → Fin de partida.

- **Menú principal:** ofrece DISTORSION (abre la pantalla "NIVELES" para elegir BROTE o Cuarto de pruebas), Ajustes y Salir.
- **Cargando:** se carga la escena del nivel; cualquier otra petición se ignora, y si la carga falla se vuelve al estado anterior.
- **Inicio de partida:** Tannat aparece en la Sala de Contención con vida completa, 500 puntos y la pistola; las puertas están cerradas. La primera ronda empieza a los 3 s.
- **Combate activo:** los mutantes aparecen en las zonas abiertas cercanas a Tannat. El jugador puede moverse, disparar, recargar y comprar durante la ronda.
- **Transición entre rondas:** cuando no quedan mutantes de la ronda vivos ni pendientes, hay 10 s de descanso. La siguiente ronda aumenta la cantidad, la vida y la velocidad.
- **Pausa:** congela el juego; clic (u Options en el mando) reanuda y Q vuelve al menú.
- **Fin de partida:** en BROTE, al caer sin RESPALDO (derrota); en el Cuarto de pruebas, al despejar la última arena (pantalla de resultados con tiempo, bajas, puntos y mejor estilo). R reinicia el nivel y Q vuelve al menú.

## Transiciones

| Estado origen | Evento | Estado destino | Condición |
| --- | --- | --- | --- |
| Menú principal | Elegir un nivel | Cargando | — |
| Cargando | Termina la carga | Jugando (inicio de partida) | — |
| Combate activo | Muere el último mutante de la ronda | Transición entre rondas | No quedan mutantes de la ronda vivos ni pendientes |
| Transición entre rondas | Pasan 10 s | Combate activo (ronda + 1) | — |
| Jugando | Pulsar Esc | Pausa | — |
| Pausa | Clic u Options | Jugando | — |
| Pausa | Pulsar Q | Menú principal | Se pierde el progreso |
| Combate activo | La vida de Tannat llega a 0 con RESPALDO | Combate activo | Tannat se reinicia y pierde RESPALDO y la última pila |
| Combate activo | La vida de Tannat llega a 0 sin RESPALDO | Fin de partida (derrota) | — |
| Fin de partida | Pulsar R | Cargando (mismo nivel) | Se reinicia todo |
| Fin de partida | Pulsar Q | Menú principal | — |

## Reglas globales

1. El progreso de la partida nunca se guarda: al reintentar se vuelve a la ronda 1 con la pistola y 500 puntos, sin mejoras ni pilas y con las puertas cerradas.
2. BROTE no tiene ronda final ni condición de victoria.
3. Los mutantes conocen la posición de Tannat desde que aparecen y solo aparecen en zonas abiertas.
4. La dificultad depende de la ronda, no de la zona.
5. Toda compra requiere puntos suficientes; si faltan, no se realiza.
6. Tannat solo puede portar dos armas y cuatro pilas a la vez.
7. Nunca hay más de 32 mutantes vivos a la vez.

## Casos especiales

Documenta excepciones importantes para evitar interpretaciones diferentes durante la implementación.

- Cambiar de arma durante una recarga la cancela sin añadir munición.
- Comprar un arma con las dos ranuras ocupadas reemplaza el arma en la mano.
- Si el jugador ya posee el arma de un soporte, compra su munición por la mitad del precio del arma; si está mejorada, ese precio se multiplica por su nivel de mejora + 1 (MK1 ×2, MK2 ×3, MK3 ×4, MK4 ×5).
- Si faltan puntos, la compra no se realiza y aparece "Puntos insuficientes".
- Antes de abrir una puerta, los mutantes no pueden aparecer en la zona que cierra.
- Se puede comprar durante el combate, no solo en el descanso.
- Si Tannat sale del área jugable, reaparece dentro del mapa.
- Al bajar por un conducto, el incinerador se convierte en el punto de reaparición.
- La pared trituradora del incinerador quita 100 de vida: sin BLINDAJE ni RESPALDO, la partida termina.
- Salir desde la pausa mantiene el nivel congelado hasta que termina la transición.

> **Navegación:** [[00 - Índice]] · ← [[06 - Economía y Recursos]] · [[01 - Premisa y Trama]] →
