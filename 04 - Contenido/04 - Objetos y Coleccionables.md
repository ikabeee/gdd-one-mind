# Objetos y Coleccionables

## Descripción de la sección

Define objetos que el jugador puede recoger, utilizar, equipar, vender, intercambiar o descubrir.

## Catálogo de armamento

### Armas

**Tipo:**  
Armas equipables.

**Descripción:**  
El juego tiene nueve armas. Las balas llegan al instante (hitscan). El Subfusil es la antigua SMG de este documento.

**Función:**  
Eliminar mutantes y permitir distintas formas de afrontar la distancia y la cantidad de enemigos.

**Cómo se obtiene:**  
La pistola se entrega al iniciar. El Rifle, la Escopeta, el Rifle de asalto, la Escopeta de bomba y la Ametralladora se compran en la pared de su zona; el Blaster, el Subfusil y el Rifle de tirador solo salen de la impresora 3D.

**Cómo se utiliza:**  
Clic izquierdo para disparar, R para recargar y 1/2 o rueda del mouse para cambiar de arma.

**Cantidad máxima:**  
Dos armas equipadas al mismo tiempo.

**Valor:**  
De 0 a 2,000 puntos según el arma (tabla de abajo).

**Rareza:**  
No se ha establecido un sistema de rarezas.

**Restricciones:**  
Se necesita munición para disparar y puntos para comprar. Con ambas ranuras ocupadas, una compra reemplaza el arma activa. Volver a usar la compra de pared de un arma que ya se tiene repone su munición (ver [[#Mejoras]]).

**Interacciones:**  
Combate, inventario, economía y acceso a las zonas.

**Representación visual:**  
Modelos 3D low poly en blanco y negro con un pequeño detalle de color. Renders en [[06 - Galería de Arte]].

| Arma | Disparo | Dónde se consigue | Costo |
|---|---|---|---:|
| Pistola | Semiautomático | Arma inicial | 0 |
| Rifle | Semiautomático | Pared · Sala de Contención | 500 |
| Escopeta | 8 perdigones, doble cañón | Pared · Sala de Contención | 500 |
| Blaster | Semiautomático, disparo de energía | Solo impresora 3D | 750 |
| Rifle de asalto | Automático | Pared · pasarela del Laboratorio Central | 1,000 |
| Subfusil | Automático | Solo impresora 3D | 1,250 |
| Escopeta de bomba | 9 perdigones, de bomba | Pared · Morgue | 1,250 |
| Rifle de tirador | Semiautomático, con mira | Solo impresora 3D | 1,500 |
| Ametralladora | Automático | Pared · Celdas | 2,000 |

> [!warning] Recortado para la entrega (2026-11-12)
> El Cohete salió del nivel para la entrega; su asset, su código y sus pruebas siguen en el proyecto. Ver [[05 - Gestión de Cambios]].

## Mejoras

La reposición de munición y la impresora 3D se compran con puntos (E) y se pierden al terminar la partida. Las pilas y los power-ups tienen sus propias secciones más abajo. No hay compra de armadura ni de vida: la vida se regenera sola (ver [[02 - Mecánicas]]) y la pila BLINDAJE sube la vida máxima.

| Mejora | Dónde | Costo | Efecto |
|---|---|---:|---|
| Reponer munición | La compra de pared del arma | Mitad del precio del arma | Llena la munición de esa arma. |
| Impresora 3D | Laboratorio Central | 950 | Un arma al azar. |
| Interruptor del stomp | Celdas | Gratis | Suelta un power-up al azar. |

### Reponer munición

**Cómo se obtiene:** Usando otra vez la compra de pared de un arma que ya se tiene y que no está llena.

**Valor:** La mitad del precio del arma, sin multiplicador: ya no hay niveles de mejora. La tabla completa está en [[06 - Economía y Recursos]].

### Estaciones de mejora (MK)

> [!warning] Recortado para la entrega (2026-11-12)
> Las estaciones de mejora (Pack-a-Punch) se quitaron para la entrega junto con la llave del incinerador, los ductos y la zona de trituración. Ver [[05 - Gestión de Cambios]].

### Impresora 3D

Es la caja misteriosa del juego. Imprime a la vista, en el suelo del Laboratorio Central: el pórtico y el cabezal barren, la cama baja y la pieza crece por capas.

**Valor:** 950 puntos por uso.

**Cómo se utiliza:** Al pagar («E  imprimir arma  [950]»), imprime durante 3 s y ofrece el arma durante 8 s («E  tomar <arma>»). Si el jugador ya lleva las 8 armas del bombo, devuelve los puntos.

**Ubicación:** una sola, fija en el suelo del Laboratorio Central.

**Contenido:** una de 8 armas al azar (Rifle, Escopeta, Blaster, Subfusil, Rifle de asalto, Escopeta de bomba, Ametralladora y Rifle de tirador), nunca una que el jugador ya lleve. No falla ni se mueve de sitio.

### Arnés Exo

> [!warning] Recortado para la entrega (2026-11-12)
> La estación del arnés Exo se quitó para la entrega. Ver [[05 - Gestión de Cambios]].

### Interruptor del stomp y orbes de dash

**Interruptor del stomp (Celdas):** Un stomp con potencia de 0.35 o más hunde la celda y suelta un power-up al azar. La celda vuelve a subir a los 20 s; el interruptor tiene un enfriamiento de 60 s.

> [!warning] Recortado para la entrega (2026-11-12)
> Los orbes de dash de la Rotonda y de Pruebas Exo se quitaron para la entrega. Ver [[05 - Gestión de Cambios]].

## Pilas de Tannat

Las pilas sustituyen a los perks de los zombies clásicos con una ficción propia. El laboratorio tiene **estaciones de carga**, una por pila, y Tannat las instala en una **bahía de 4 ranuras** que lleva en el panel del costado, el de la luz roja. Cada pila da una ventaja mientras siga instalada.

**Tipo:** Mejora comprable e instalable.

**Cómo se obtiene:** Comprándola con puntos en su estación de carga (E). El nivel tiene una estación por pila.

**Cómo se utiliza:** Se aplica en cuanto se instala y dura hasta el final de la partida o hasta que un reinicio de RESPALDO la queme.

**Cantidad máxima:** 4 pilas instaladas a la vez, de un catálogo de 7. Ninguna se repite.

**Valor:** 2,000 puntos más 500 por cada pila ya instalada (2,000, 2,500, 3,000 y 3,500). RESPALDO cuesta siempre 500.

**Rareza:** No aplica; todas están siempre a la venta.

**Restricciones:** Con la bahía llena no se puede instalar otra. RESPALDO solo puede instalarse 3 veces por partida. Una máquina que no puede vender no muestra texto; al pulsar E se escucha el barrido de la mano y Cuyus pone cara de rechazo.

**Interacciones:** Vida, regeneración, armas, movimiento, economía y la derrota (RESPALDO).

**Representación visual:**
- **En el HUD:** 4 ranuras con forma de pila debajo del retrato de Tannat. Una ranura con pila se llena con su color y su icono de 7×7 píxeles; una vacía es solo un contorno, así que el límite siempre está a la vista.
- **En el cuerpo de Tannat:** celdas cilíndricas con una banda de color que brilla en la bahía del costado. Aún no está modelada; se usa como referencia para el tráiler.

| Pila | Ventaja | Color / icono |
| --- | --- | --- |
| **BLINDAJE** | Vida máxima de 100 a 160: aguanta un golpe más antes de caer (los mutantes pegan 40). | Rojo / hexágono |
| **RÁFAGA** | Cadencia ×1.25, sin bono de daño. | Naranja / triángulo |
| **SERVO** | Recarga ×0.7. | Verde / engrane |
| **PISTÓN** | Correr, deslizarse y el dash ×1.1; enfriamiento del deslizamiento y del stomp ×0.6. | Amarillo / doble flecha |
| **RESPALDO** | Si Tannat cae, se reinicia en 3 s en lugar de perder. El reinicio quema RESPALDO y la última pila instalada; las demás se quedan. | Rosa / corazón (el del vestido de Cuyus) |
| **FILTRO** | La vida empieza a regenerarse a los 1.25 s sin daño en vez de 2.5 s, y regenera ×1.5 más rápido. Protege a Cuyus del virus (solo narrativa). | Blanco turquesa / rejilla |
| **DESCARGA** | Al empezar una recarga, Tannat suelta una descarga eléctrica de 1 a 4 m y de 150 a 600 de daño, más grande cuanto más vacío estaba el cargador. Una vez cada tiempo de recarga + 3 s. | Violeta / rayo |

> [!note] Texto en el juego
> La fuente pixel del juego no dibuja acentos, así que dentro del juego los nombres y textos van sin ellos (RAFAGA, PISTON, «Bahia», «mas rapido»). Este documento y el tráiler conservan RÁFAGA y PISTÓN.

## Power-ups

Al morir, un mutante puede soltar un power-up que flota sobre el suelo. Tannat lo recoge al pasar encima.

**Tipo:** Consumible de efecto inmediato o temporal.

**Cómo se obtiene:**
- Cada baja tiene un 3 % de probabilidad de soltar uno, con un máximo de 4 por ronda.
- Ganar suficientes puntos garantiza que la siguiente baja suelte uno. El primero llega a los 2,500 puntos ganados; después, cada 2,000 puntos, cantidad que crece ×1.14 tras cada drop garantizado.
- El tipo sale de una bolsa barajada: aparecen todos antes de repetir uno.
- Durante una PURGA no cae nada.
- El interruptor del stomp de las Celdas suelta uno de la misma bolsa, fuera del límite por ronda.

**Cómo se utiliza:** Al pasar por encima. Si se recoge otra vez un efecto temporal que ya está activo, su tiempo vuelve a empezar.

**Cantidad máxima:** No se acumulan; un efecto activo solo renueva su tiempo.

**Valor:** Gratis.

**Rareza:** Todos tienen la misma probabilidad, por la bolsa.

**Restricciones:** Un power-up en el suelo dura 30 s: 18 s fijo y 12 s parpadeando a 3 velocidades (6 s lento, 4 s medio y 2 s rápido) antes de desaparecer.

**Interacciones:** Puntos, combate, munición y movimiento.

**Representación visual:** Una gema que gira y flota. Al recoger un efecto temporal aparece su icono blanco de 7×7 píxeles abajo al centro, sobre «RESTANTES»: fijo mientras dura y parpadeante los últimos 5 s (más rápido los últimos 2 s). Al recoger PURGA o MUNICION MAXIMA aparece su mensaje en pantalla durante 2.5 s.

| Power-up | Efecto | Duración |
| --- | --- | --- |
| **PUNTOS DOBLES** | Los puntos ganados valen el doble. | 30 s |
| **LETAL** | Cualquier impacto mata a cualquier mutante. | 30 s |
| **PURGA** | La descontaminación del laboratorio mata a todos los mutantes vivos. Da 400 puntos fijos y sus bajas no dan puntos. | Inmediato |
| **MUNICIÓN** | Llena cargadores y reservas de todas las armas. | Inmediato |
| **IMPULSO** | Salto ×1.5, velocidad ×1.25, un salto extra en el aire y enfriamientos ×0.5. Al recogerlo deja listos de inmediato el deslizamiento, el stomp y el dash. | 30 s |


> **Navegación:** [[00 - Índice]] · ← [[03 - Enemigos y NPC]] · [[05 - Misiones y Desafíos]] →
