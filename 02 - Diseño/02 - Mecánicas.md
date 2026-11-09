# Mecánicas

## Descripción de la sección

Una mecánica es una regla o interacción mediante la cual el jugador puede actuar dentro del sistema del juego.

Documenta cada mecánica con suficiente detalle para que otro integrante pueda implementarla.

> [!info] Fuente de los valores
> Los números de esta página son los valores actuales del juego, definidos en los ScriptableObjects de `Assets/_Game/Data/` del repositorio del juego. Si cambian allá, se actualizan aquí.

## Mecánicas principales

### Mecánica 01 — Movimiento con exotraje

**Propósito:**  
Permitir que Tannat mantenga distancia, cambie de posición, use la altura del mapa y convierta el movimiento en ataque.

**Activación:**  
El jugador corre, salta, hace dash, se desliza (slide) o cae en picada (stomp).

**Reglas:**  
- **Correr:** 13 m/s, sin estamina.
- **Salto:** 4 m de altura, con un salto extra en el aire (doble salto).
- **Dash:** impulso de 45 m/s durante 0.15 s; una carga que se recupera al tocar el suelo; hace 200 de daño a los mutantes que atraviesa.
- **Slide:** en el suelo, 18 m/s que se pierden con la fricción; acelera en pendientes.
- **Stomp:** en el aire, Tannat cae a 70 m/s; al impactar hace de 150 a 600 de daño en un radio de 3 a 6 m (más caída, más fuerza) y rebota hacia arriba. Enfriamiento de 1.5 s.
- **Orbes de dash:** orbes flotantes en el Laboratorio Central y en Pruebas Exo; al tocarlos se recuperan el dash, los saltos aéreos y el stomp, igual que con una baja. Cada orbe reaparece a los 2 s. Sirven para encadenar dashes sobre huecos largos.
- **Explosiones:** el cohete no daña a Tannat y su explosión lo empuja (una vez por salto, con tope de 45 m/s).

**Entrada:**  
W, A, S, D para desplazarse; Espacio para saltar; Shift izquierdo para dash; Ctrl izquierdo o C para slide (en el suelo) o stomp (en el aire); mouse para orientar la cámara.

**Estado inicial:**  
Tannat en reposo o desplazándose.

**Estado final:**  
Tannat reposicionado y, si atravesó o aplastó mutantes, con daño aplicado.

**Recursos utilizados:**  
Ninguno; solo cargas y enfriamientos (dash, stomp, slide).

**Recompensa:**  
Evasión de daño, mejor posición y bajas en movimiento (130 puntos y más estilo).

**Penalización:**  
Un mal uso puede dejar a Tannat expuesto a la horda o fuera de una plataforma.

**Interacciones con otras mecánicas:**  
Se puede disparar y recargar mientras se corre o se salta. La pila PISTÓN y el power-up IMPULSO mejoran el movimiento; el arnés del hangar da un salto aéreo extra.

**Casos límite:**  
Las colisiones impiden atravesar paredes. Un stomp atorado en una pendiente empinada termina solo. Si Tannat sale del área jugable, reaparece dentro del mapa.

### Mecánica 02 — Disparo / Combate

**Propósito:**  
Es la acción principal para eliminar mutantes, avanzar de ronda y ganar puntos.

**Activación:**  
Apuntar con clic derecho (miras de hierro o mira telescópica), disparar con clic izquierdo y recargar con R.

**Reglas:**  
Todas las balas son instantáneas (hitscan), excepto el cohete, que es un proyectil con explosión. Se pueden portar dos armas a la vez. Hay diez armas (ver [[04 - Objetos y Coleccionables]]); cada una tiene daño, cadencia, cargador y reserva propios. Hay asistencia de apuntado con alcance distinto por arma. Los disparos a la cabeza dan más puntos.

**Entrada:**  
Clic izquierdo para disparar, clic derecho para apuntar, R para recargar, 1, 2 o rueda del mouse para cambiar de arma, G para soltar el arma.

**Estado inicial:**  
Arma equipada lista para disparar.

**Estado final:**  
Se descuenta munición y, si el disparo impacta, se aplica daño. Las escopetas disparan 8 o 9 perdigones.

**Recursos utilizados:**  
Munición del arma equipada.

**Recompensa:**  
10 puntos por impacto y de 60 a 130 por baja.

**Penalización:**  
Agotar el cargador obliga a recargar; agotar la reserva obliga a comprar munición, recoger MUNICIÓN MÁXIMA o usar la otra arma.

**Interacciones con otras mecánicas:**  
Depende de la compra de armas y de la economía. Las mejoras de arma multiplican el daño; las pilas RÁFAGA, SERVO y DESCARGA cambian la cadencia y la recarga.

**Casos límite:**  
Cambiar de arma durante una recarga la cancela sin añadir munición. Si ambas ranuras están ocupadas, comprar otra arma reemplaza la que está en la mano.

### Mecánica 03 — Compras e interacción

**Propósito:**  
Traduce el desempeño en combate (puntos) en equipo y en más mapa disponible.

**Activación:**  
Acercarse a un punto de compra y pulsar E con los puntos necesarios.

**Reglas:**  
- **Armas de pared:** cada zona tiene una o dos. Si ya tienes el arma, compras su munición a la mitad del precio del arma; si está mejorada, ese precio se multiplica por su nivel de mejora + 1 (MK1 ×2, MK2 ×3, MK3 ×4, MK4 ×5).
- **Impresora 3D (caja misteriosa):** 950 puntos; imprime un arma al azar que no llevas y tienes un tiempo para tomarla. Si la impresión falla, devuelve los puntos y se mueve a otra de sus cinco ubicaciones.
- **Puertas:** cada puerta se paga una vez y queda abierta hasta terminar la partida.
- **Estaciones de mejora:** mejoran el arma en mano un nivel y la recargan.
- **Pilas:** se instalan en Tannat en las estaciones de carga.
- **Trampas, arnés y conductos:** ver [[03 - Sistemas]].

**Entrada:**  
Tecla E frente al objeto interactuable.

**Estado inicial:**  
Puntos disponibles; compra aún no realizada.

**Estado final:**  
Se descuentan los puntos y se entrega la compra.

**Recursos utilizados:**  
Puntos.

**Recompensa:**  
Mejor equipo o acceso a otra zona.

**Penalización:**  
Gastar puntos que ya no estarán disponibles para otra compra en esa misma partida.

**Interacciones con otras mecánicas:**  
Alimenta directamente el disparo (armas y mejoras), la supervivencia (pilas) y el movimiento (zonas y arnés).

**Casos límite:**  
Si faltan puntos, no se realiza la compra y aparece "Puntos insuficientes". Cada puerta solo se cobra una vez.

## Mecánicas secundarias

Lista las mecánicas que complementan la experiencia pero no constituyen el núcleo.

- **Regeneración de vida:** Tannat tiene 100 de vida; tras 2.5 s sin recibir daño recupera 60 por segundo.
- **Power-ups:** los mutantes los sueltan al azar (ver [[03 - Sistemas]]).
- **Medidor de estilo:** dañar y eliminar llena el medidor, el tiempo y los golpes recibidos lo vacían; los rangos son D, C, B, A y S.
- **Interruptor de pisotón:** en las Celdas, un stomp lo bastante fuerte hunde la celda exterior y suelta un power-up al azar.
- **Incinerador secreto:** se baja por un conducto (500 puntos); ahí está la llave que desbloquea la mejora experimental, mientras una pared trituradora avanza. Si la pared alcanza a Tannat le quita 100 de vida: sin BLINDAJE ni RESPALDO, la partida termina.

> **Navegación:** [[00 - Índice]] · ← [[01 - Jugabilidad]] · [[03 - Sistemas]] →
