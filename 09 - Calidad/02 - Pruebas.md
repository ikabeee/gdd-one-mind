# Pruebas

## Descripción de la sección

Define cómo se comprobará que el videojuego funciona como fue diseñado.

## Tipos de prueba

### Pruebas funcionales

Comprueban que una característica haga lo que debe.

Movimiento (salto, doble salto, deslizamiento, dash y stomp), disparo y recarga de cada arma, cambio de arma, compras, apertura de la puerta, mejoras, derrota y reintentar.

### Pruebas de integración

Comprueban que varios sistemas funcionen correctamente juntos.

Baja de un mutante → suma de puntos → conteo de la ronda. Compra → descuento de puntos → HUD actualizado. Apertura de la puerta → aparición de mutantes en la Zona 2.

### Pruebas de usabilidad

Comprueban si los jugadores entienden y pueden utilizar el sistema.

Playtests con jugadores del público objetivo (18 a 25 años) que no conozcan el juego: ¿entienden cómo comprar y abrir la puerta sin ayuda? ¿Entienden por qué perdieron?

### Pruebas de rendimiento

Comprueban FPS, memoria, tiempos de carga y estabilidad.

Medir FPS con distintas cantidades de enemigos activos en equipos de gama media para comprobar el límite de 32 mutantes vivos. Sesiones largas (más de 15 minutos) para revisar estabilidad.

## Casos de prueba

### Compra sin puntos suficientes

**Objetivo:** Comprobar que no se puede comprar sin puntos.

**Precondiciones:** Partida con menos de 500 puntos (por ejemplo, después de comprar el Rifle).

**Pasos:**

1. Acercarse a la compra de pared de la Escopeta, en la Sala de Contención.
2. Pulsar E.

**Resultado esperado:** No se realiza la compra; el costo parpadea en rojo y suena un rechazo. Los puntos no cambian.

**Resultado obtenido:**

**Estado:** Correcto / Incorrecto

### Apertura de la puerta

**Objetivo:** Comprobar que la puerta 2 se cobra una vez y habilita la Zona 2 (Laboratorio Central).

**Precondiciones:** Partida iniciada con al menos 1,250 puntos.

**Pasos:**

1. Acercarse a la puerta 2 y pulsar E.
2. Volver a pulsar E frente a la puerta abierta.
3. Esperar a la siguiente ronda.

**Resultado esperado:** Se descuentan 1,250 puntos una sola vez, la puerta queda abierta y empiezan a aparecer mutantes en la Zona 2.

**Resultado obtenido:**

**Estado:** Correcto / Incorrecto

### Cambio de arma durante la recarga

**Objetivo:** Comprobar que cambiar de arma cancela la recarga.

**Precondiciones:** Dos armas equipadas y cargador incompleto.

**Pasos:**

1. Pulsar R para recargar.
2. Antes de que termine, pulsar 2.
3. Volver al arma anterior con 1.

**Resultado esperado:** La recarga se cancela y el cargador conserva la munición que tenía antes de recargar.

**Resultado obtenido:**

**Estado:** Correcto / Incorrecto

### Derrota y reintentar

**Objetivo:** Comprobar que reintentar reinicia todo el progreso.

**Precondiciones:** Partida con armas compradas, mejoras, sin RESPALDO y con la Zona 2 abierta.

**Pasos:**

1. Dejar que la vida de Tannat llegue a 0.
2. Revisar la pantalla de derrota.
3. Pulsar R (o X / botón sur en el mando).

**Resultado esperado:** La pantalla "GAME OVER" muestra las rondas sobrevividas ("Sobreviviste N rondas"). La nueva partida empieza en la ronda 1, Sala de Contención, con la pistola, 500 puntos, sin pilas y con las puertas cerradas.

> [!warning] Recortado para la entrega (2026-11-12)
> La pantalla «HAS CAIDO» quedó reemplazada por "GAME OVER". Ver [[05 - Gestión de Cambios]].

**Resultado obtenido:**

**Estado:** Correcto / Incorrecto

## Pendiente de verificar en la entrega (2026-11-12)

- Partida completa en la build: recorrido de Sala de Contención y Morgue, Rotonda tras el arnés, gap de 2 s y máquinas silenciosas.
- Apertura y costura del menú; pasos, ambiente y murmullo de la horda en juego.
- Rendimiento en player standalone y en Windows; 60 FPS sin comprobar.
- `ShutdownBodyPlayTests` (falla intermitente, un caso distinto cada vez).


> **Navegación:** [[00 - Índice]] · ← [[01 - Criterios de Calidad]] · [[03 - Bugs y Seguimiento]] →
