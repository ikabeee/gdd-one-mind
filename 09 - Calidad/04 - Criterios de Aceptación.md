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

**Entonces:** se descuenta el costo, el arma ocupa la ranura libre (o reemplaza la que está en la mano si ambas están ocupadas) y el HUD se actualiza.

### Apertura de una zona

**Dado que:** el jugador tiene los puntos de la puerta (750 a 1,250) y la puerta está cerrada.

**Cuando:** pulsa E frente a la puerta.

**Entonces:** se descuenta el costo una sola vez, la puerta queda abierta hasta terminar la partida y se habilitan los puntos de aparición de esa zona.

### Fin de ronda

**Dado que:** no quedan mutantes vivos ni pendientes de aparecer.

**Cuando:** muere el último mutante.

**Entonces:** comienzan 10 s de descanso y después una ronda con más mutantes, con más vida y más rápidos.

### Derrota

**Dado que:** la partida está en curso.

**Cuando:** la vida de Tannat llega a 0 sin una pila RESPALDO.

**Entonces:** se desactiva el control, aparece "HAS CAIDO" con el progreso, las bajas y los puntos, y se puede repetir (R) o volver al menú (Q).

## Criterios del proyecto

- [x] El bucle principal funciona: combatir, ganar puntos, comprar y pasar de ronda.
- [x] La condición de derrota funciona (en BROTE no hay condición de victoria: modo endless).
- [x] Reintentar reinicia todo el progreso (no hay guardado de partida).
- [x] Los sistemas principales están integrados: armas, IA, rondas, economía y zonas.
- [x] Las pruebas críticas están aprobadas (suite automatizada en verde el 2026-11-05).
- [ ] El rendimiento cumple el objetivo definido: 60 FPS en equipos de gama media.
- [ ] No existen errores bloqueantes conocidos.


> **Navegación:** [[00 - Índice]] · ← [[03 - Bugs y Seguimiento]] · [[01 - Glosario]] →
