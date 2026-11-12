# Mecánicas

## Descripción de la sección

Una mecánica es una regla o interacción mediante la cual el jugador puede actuar dentro del sistema del juego.

Documenta cada mecánica con suficiente detalle para que otro integrante pueda implementarla.

## Mecánicas principales

### Mecánica 01 — Movimiento

**Propósito:**  
Permitir que Tannat mantenga distancia, cambie de posición y recorra el escenario durante el combate.

**Activación:**  
El jugador corre, salta, se desliza, hace dash o stomp.

**Reglas:**  
Tannat corre siempre a 13 m/s: no hay caminar ni sprint aparte. Acelera a 100 m/s² y frena a 80 m/s², y su velocidad máxima es de 30 m/s.

| Movimiento | Entrada (teclado / mando) | Reglas |
|---|---|---|
| Correr | W, A, S, D / stick izquierdo | 13 m/s constantes. |
| Salto | Espacio / botón sur | Alcanza 4 m de altura en 0.49 s. *Coyote time* de 0.1 s (todavía puede saltar 0.1 s después de dejar un borde) y búfer de 0.1 s (un salto pulsado justo antes de aterrizar se ejecuta al tocar el suelo). |
| Doble salto | Espacio en el aire | 1 salto en el aire, unos 8 m de altura en total. |
| Deslizamiento | Ctrl izquierdo o C al correr en el suelo / botón este | 18 m/s con un impulso de +8 m/s durante 0.5 s. Dura al menos 0.45 s, termina por debajo de 6 m/s y tiene un enfriamiento de 0.6 s. Saltar mientras se desliza da ×1.25 de altura y +2 m/s. |
| Dash | Shift izquierdo / LB | En el suelo y en el aire: 45 m/s durante 0.15 s. 1 carga con enfriamiento de 0.3 s; se recarga al aterrizar y al matar. Golpea por 200 de daño o el 60 % de la vida máxima del objetivo, y da 0.3 s de invulnerabilidad. |
| Stomp | Ctrl izquierdo o C en el aire / RB | Solo en el aire: cae a 70 m/s y hace de 150 a 600 de daño (o del 35 al 100 % de la vida del objetivo) en un radio de 3 a 6 m. Alcanza la potencia máxima tras 0.3 s de caída. Enfriamiento de 1.5 s; rebota 5 m sobre una cabeza (7 m si se salta) y da 0.5 s de invulnerabilidad al aterrizar. |

El daño del dash y del stomp depende de la velocidad: ×0.75 quieto, ×1 corriendo y ×1.5 a la velocidad máxima.

No existen agacharse, trepar bordes, correr por paredes ni ataque cuerpo a cuerpo.

**Entrada:**  
W, A, S y D para desplazarse; Espacio para saltar; Ctrl izquierdo o C para deslizarse (en el suelo) o hacer stomp (en el aire); Shift izquierdo para el dash; movimiento del mouse para orientar la cámara. El mando se describe en [[04 - Controles]].

**Estado inicial:**  
Tannat en reposo o desplazándose a ritmo base.

**Estado final:**  
Tannat reposicionado, habiendo evadido o alcanzado una posición de combate ventajosa.

**Recursos utilizados:**  
Ninguno; el movimiento no consume energía ni estamina. El deslizamiento, el dash y el stomp tienen enfriamiento, y el dash tiene una carga.

**Recompensa:**  
Evasión de daño, mejor posicionamiento táctico y bajas con el dash o el stomp, que dan más puntos.

**Penalización:**  
Ninguna directa; un mal uso puede dejar a Tannat expuesto a los mutantes.

**Interacciones con otras mecánicas:**  
Es posible disparar y recargar mientras se corre o salta, sin reducir la velocidad.

**Casos límite:**  
Las colisiones deben impedir atravesar paredes y evitar que Tannat quede suspendido o atascado al saltar contra bordes.

### Mecánica 02 — Disparo / Combate

**Propósito:**  
Es la acción principal para eliminar mutantes, avanzar de ronda y ganar puntos.

**Activación:**  
Apuntar con la mira central, disparar con clic izquierdo y recargar con R.

**Reglas:**  
El catálogo tiene nueve armas (ver [[04 - Objetos y Coleccionables]]); se pueden portar dos a la vez. La pistola inicial es semiautomática. Las balas llegan al instante (hitscan). Las escopetas disparan perdigones (8 la Escopeta y 9 la Escopeta de bomba).

**Entrada:**  
Clic izquierdo para disparar, R para recargar, teclas 1 y 2 o rueda del mouse para cambiar de arma.

**Estado inicial:**  
Arma equipada lista para disparar.

**Estado final:**  
Se descuenta munición y, si el disparo impacta, se aplica daño al mutante. Las escopetas disparan varios perdigones en forma de cono.

**Recursos utilizados:**  
Munición del arma equipada.

**Recompensa:**  
Puntos al eliminar mutantes.

**Penalización:**  
Agotar el cargador obliga a recargar; agotar la reserva requiere reabastecerse o usar la otra arma.

**Interacciones con otras mecánicas:**  
Depende de la compra de armas y del sistema de economía; se combina con el movimiento.

**Casos límite:**  
Cambiar de arma durante una recarga la cancela sin añadir munición. Si ambas ranuras están ocupadas, comprar otra arma reemplaza la activa. Estas reglas deben mantenerse iguales en todas las armas.

### Mecánica 03 — Compra de armas, munición, pilas y puertas

**Propósito:**  
Traduce el desempeño en combate (puntos) en equipo y en expansión del mapa disponible.

**Activación:**  
Acercarse a un punto de compra y pulsar E con los puntos necesarios.

**Reglas:**  
Cada zona abierta tiene sus compras de pared (ver [[02 - Niveles]]). Tres puertas conectan las zonas de BROTE; cada una permanece abierta después del pago hasta terminar la partida. Si el jugador ya posee el arma de la pared y no está llena, la misma compra repone su munición (precio en [[06 - Economía y Recursos]]).

**Entrada:**  
Tecla E frente al objeto interactuable.

**Estado inicial:**  
Puntos disponibles, arma/power-up/zona aún no adquirida.

**Estado final:**  
Se descuentan los puntos y se equipa el arma, se repone munición, se instala la pila o se abre la puerta.

**Recursos utilizados:**  
Puntos.

**Recompensa:**  
Mejor equipamiento o acceso a nuevas zonas, que ofrecen más espacio para moverse.

**Penalización:**  
Gastar puntos que ya no estarán disponibles para otra compra en esa misma partida.

**Interacciones con otras mecánicas:**  
Alimenta directamente el disparo (armas) y el movimiento/exploración (zonas).

**Casos límite:**  
Si faltan puntos, no se realiza la compra; el costo parpadea en rojo y se reproduce un sonido de rechazo. Cada puerta solo se cobra una vez.

### Mecánica 04 — Vida de Tannat

**Propósito:**  
Medir cuánto castigo aguanta Tannat y premiar que salga un momento del combate.

**Activación:**  
Recibir daño de los mutantes.

**Reglas:**  
Tannat tiene 100 de vida. Tras 2.5 s sin recibir daño empieza a regenerarse a 60 de vida por segundo. Recibir un golpe no da invulnerabilidad: un mutante quita 40 por golpe, así que tres golpes seguidos lo derriban. La pila BLINDAJE sube la vida máxima a 160 y FILTRO acelera la regeneración.

**Estado final:**  
Si Tannat cae con RESPALDO instalado, se reinicia con 2 s de invulnerabilidad; si cae sin RESPALDO, la partida termina.

## Mecánicas secundarias

Lista las mecánicas que complementan la experiencia pero no constituyen el núcleo.

- **Mejoras:** reponer munición en la pared y la impresora 3D (ver [[04 - Objetos y Coleccionables]]).
- **Pilas y power-ups:** 4 pilas instaladas de un catálogo de 7, y 5 power-ups que sueltan los mutantes.
- **Trampas:** el anillo electrificado; 1,000 puntos, activo 20 s. Sus bajas no dan puntos.
- **Rango de estilo:** de D a S; multiplica los puntos ganados de ×1 a ×2.5 (ver [[06 - Economía y Recursos]]).


> **Navegación:** [[00 - Índice]] · ← [[01 - Jugabilidad]] · [[03 - Sistemas]] →
