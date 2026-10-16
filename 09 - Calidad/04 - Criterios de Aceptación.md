# Criterios de Aceptación

## Descripción de la sección

Los criterios de aceptación permiten decidir objetivamente si una característica está lista.

## Plantilla

### Característica

**Dado que:** <!-- contexto inicial -->

**Cuando:** <!-- acción -->

**Entonces:** <!-- resultado esperado -->

## Características

### Compra de armas

**Dado que:** el jugador tiene puntos suficientes y está frente a un soporte de arma.

**Cuando:** pulsa E.

**Entonces:** se descuenta el costo, el arma ocupa la ranura libre (o reemplaza la activa si ambas están ocupadas) y el HUD se actualiza.

### Apertura de la Zona 2

**Dado que:** el jugador tiene al menos 1,250 puntos y la puerta está cerrada.

**Cuando:** pulsa E frente a la puerta.

**Entonces:** se descuenta el costo una sola vez, la puerta queda abierta hasta terminar la partida y se habilitan los puntos de aparición de la Zona 2.

### Fin de ronda

**Dado que:** no quedan mutantes vivos ni pendientes de aparecer.

**Cuando:** muere el último mutante.

**Entonces:** comienza la transición entre rondas y después una ronda con más mutantes y con más vida.

### Derrota

**Dado que:** la partida está en curso.

**Cuando:** la vida de Tannat llega a 0.

**Entonces:** se desactiva el control y se muestran las rondas superadas y los puntos totales, con la opción de reintentar.

## Criterios del proyecto

- [ ] El bucle principal funciona: combatir, ganar puntos, comprar y pasar de ronda.
- [ ] La condición de derrota funciona (no hay condición de victoria: modo endless).
- [ ] Reintentar reinicia todo el progreso (no hay guardado de partida).
- [ ] Los sistemas principales están integrados: armas, IA, rondas, economía y zonas.
- [ ] Las pruebas críticas están aprobadas.
- [ ] El rendimiento cumple el objetivo definido: 60 FPS en equipos de gama media.
- [ ] No existen errores bloqueantes conocidos.


> **Navegación:** [[00 - Índice]] · ← [[03 - Bugs y Seguimiento]] · [[01 - Glosario]] →
