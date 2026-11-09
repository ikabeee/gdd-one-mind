# Pruebas

## Descripción de la sección

Define cómo se comprobará que el videojuego funciona como fue diseñado.

## Tipos de prueba

### Pruebas funcionales

Comprueban que una característica haga lo que debe.

Movimiento con exotraje, disparo y recarga de cada arma, cambio de arma, compras, apertura de puertas, impresora 3D, mejoras, pilas, power-ups, trampas, derrota y reintentar.

### Pruebas de integración

Comprueban que varios sistemas funcionen correctamente juntos.

Baja de un mutante → suma de puntos → conteo de la ronda. Compra → descuento de puntos → HUD actualizado. Apertura de una puerta → aparición de mutantes en la zona nueva cuando Tannat está en ella o al lado.

### Pruebas de usabilidad

Comprueban si los jugadores entienden y pueden utilizar el sistema.

Playtests con jugadores del público objetivo (18 a 25 años) que no conozcan el juego: ¿entienden cómo comprar y abrir la puerta sin ayuda? ¿Entienden por qué perdieron?

### Pruebas de rendimiento

Comprueban FPS, memoria, tiempos de carga y estabilidad.

Medir FPS con distintas cantidades de enemigos activos en equipos de gama media para fijar el límite de enemigos. Sesiones largas (más de 15 minutos) para revisar estabilidad.

## Pruebas automatizadas

El juego tiene pruebas unitarias (una regla en C# sin escena) y de flujo completo (arrancan el juego real desde `Bootstrap` y lo juegan a través de sus servicios: iniciar, jugar, ganar, perder y volver al menú). Ambas corren en la suite EditMode del Unity Test Framework con `./run-tests.sh` o desde *Window > General > Test Runner*. El 2026-11-07 la suite completa (954 pruebas) pasó en verde.

Antes de la entrega se hizo una ronda "break the game" (intentar romper el juego) que corrigió, entre otros: mutantes que no pueden navegar, rondas que esperaban mutantes ajenos, vida infinita en rondas altas, empujes de explosión sin tope, reembolsos de movilidad por trampas y PURGA, y salir del mapa.

## Casos de prueba

### Compra sin puntos suficientes

**Objetivo:** Comprobar que no se puede comprar sin puntos.

**Precondiciones:** Partida recién iniciada (500 puntos).

**Pasos:**

1. Acercarse a la puerta de Administración (750).
2. Pulsar E.

**Resultado esperado:** No se realiza la compra y aparece "Puntos insuficientes". Los puntos no cambian.

**Resultado obtenido:**

**Estado:** Correcto / Incorrecto

### Apertura de la puerta

**Objetivo:** Comprobar que la puerta se cobra una vez y habilita el Laboratorio Central.

**Precondiciones:** Partida iniciada con al menos 1,250 puntos.

**Pasos:**

1. Acercarse a la puerta del Laboratorio Central y pulsar E.
2. Volver a pulsar E frente a la puerta abierta.
3. Entrar al Laboratorio Central y esperar a la siguiente ronda.

**Resultado esperado:** Se descuentan 1,250 puntos una sola vez, la puerta queda abierta y empiezan a aparecer mutantes en el Laboratorio Central.

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

**Precondiciones:** Partida con armas compradas, mejoras, pilas (sin RESPALDO) y puertas abiertas.

**Pasos:**

1. Dejar que la vida de Tannat llegue a 0.
2. Revisar la pantalla "HAS CAIDO".
3. Pulsar R.

**Resultado esperado:** La pantalla muestra el progreso, las bajas y los puntos. La nueva partida empieza en la ronda 1, en la Sala de Contención, con la pistola, 500 puntos, sin mejoras ni pilas y con las puertas cerradas.

**Resultado obtenido:**

**Estado:** Correcto / Incorrecto


> **Navegación:** [[00 - Índice]] · ← [[01 - Criterios de Calidad]] · [[03 - Bugs y Seguimiento]] →
