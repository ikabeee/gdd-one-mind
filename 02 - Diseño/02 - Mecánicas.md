# Mecánicas

## Descripción de la sección

Una mecánica es una regla o interacción mediante la cual el jugador puede actuar dentro del sistema del juego.

Documenta cada mecánica con suficiente detalle para que otro integrante pueda implementarla.

## Mecánicas principales

### Mecánica 01 — Movimiento básico

**Propósito:**  
Permitir que Tannat mantenga distancia, cambie de posición y recorra el escenario durante el combate.

**Activación:**  
El jugador se mueve y salta.

**Reglas:**  
La velocidad base es constante, con ritmo de carrera ligera. Solo hay un salto de altura fija, que se activa desde el suelo.

**Entrada:**  
W, A, S y D para desplazarse; Espacio para saltar; movimiento del mouse para orientar la cámara.

**Estado inicial:**  
Tannat en reposo o desplazándose a ritmo base.

**Estado final:**  
Tannat reposicionado, habiendo evadido o alcanzado una posición de combate ventajosa.

**Recursos utilizados:**  
Ninguno; el movimiento no consume energía ni estamina.

**Recompensa:**  
Evasión de daño, mejor posicionamiento táctico.

**Penalización:**  
Ninguna directa; un mal uso puede dejar a Tannat expuesto a los mutantes.

**Interacciones con otras mecánicas:**  
Es posible disparar y recargar mientras se camina o salta, sin reducir la velocidad.

**Casos límite:**  
Las colisiones deben impedir atravesar paredes y evitar que Tannat quede suspendido o atascado al saltar contra bordes.

### Mecánica 02 — Disparo / Combate

**Propósito:**  
Es la acción principal para eliminar mutantes, avanzar de ronda y ganar puntos.

**Activación:**  
Apuntar con la mira central, disparar con clic izquierdo y recargar con R.

**Reglas:**  
El catálogo incluye pistola, SMG y escopeta; se pueden portar dos armas a la vez. La pistola inicial es semiautomática y precisa; la SMG es automática, de alta cadencia y menor daño por bala; la escopeta dispara perdigones y resulta más efectiva a corta distancia.

**Entrada:**  
Clic izquierdo para disparar, R para recargar, teclas 1 y 2 o rueda del mouse para cambiar de arma.

**Estado inicial:**  
Arma equipada lista para disparar.

**Estado final:**  
Se descuenta munición y, si el disparo impacta, se aplica daño al mutante. La escopeta dispara varios perdigones en forma de cono.

**Recursos utilizados:**  
Munición del arma equipada.

**Recompensa:**  
Puntos al eliminar mutantes.

**Penalización:**  
Agotar el cargador obliga a recargar; agotar la reserva requiere reabastecerse o usar la otra arma.

**Interacciones con otras mecánicas:**  
Depende de la compra de armas y del sistema de economía; se combina con el movimiento.

**Casos límite:**  
Cambiar de arma durante una recarga la cancela sin añadir munición. Si ambas ranuras están ocupadas, comprar otra arma reemplaza la activa. Estas reglas deben mantenerse iguales en las tres armas.

### Mecánica 03 — Compra de armas, munición, mejoras y puerta

**Propósito:**  
Traduce el desempeño en combate (puntos) en mejoras y en expansión del mapa disponible.

**Activación:**  
Acercarse a un punto de compra y pulsar E con los puntos necesarios.

**Reglas:**  
La SMG se compra en la Zona 1 y la escopeta en la Zona 2. Una sola puerta conecta ambas áreas y permanece abierta después del pago hasta terminar la partida. Si el jugador ya posee el arma del soporte, puede comprar su munición por un costo menor.

**Entrada:**  
Tecla E frente al objeto interactuable.

**Estado inicial:**  
Puntos disponibles, arma/power-up/zona aún no adquirida.

**Estado final:**  
Se descuentan los puntos y se equipa el arma, se repone munición, se aplica la mejora o se abre la puerta.

**Recursos utilizados:**  
Puntos.

**Recompensa:**  
Mejor equipamiento o acceso a la Zona 2, que ofrece más espacio para moverse.

**Penalización:**  
Gastar puntos que ya no estarán disponibles para otra compra en esa misma partida.

**Interacciones con otras mecánicas:**  
Alimenta directamente el disparo (armas) y el movimiento/exploración (zonas).

**Casos límite:**  
Si faltan puntos, no se realiza la compra; el costo parpadea en rojo y se reproduce un sonido de rechazo. La puerta solo se cobra una vez.

## Mecánicas secundarias

Lista las mecánicas que complementan la experiencia pero no constituyen el núcleo.

- **Mejoras:** abastecer munición, armadura (reduce el daño recibido) y restablecer vida. Se obtienen mediante compra con puntos y complementan el combate sin ser el núcleo de la experiencia.


> **Navegación:** [[00 - Índice]] · ← [[01 - Jugabilidad]] · [[03 - Sistemas]] →
