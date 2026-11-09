# Sistemas del Juego

## Descripción de la sección

Los sistemas son conjuntos de reglas y componentes que trabajan juntos: combate, inventario, IA, diálogo, progresión, economía, misiones, etc.

## Inventario de sistemas

| Sistema | Propósito | Dependencias | Estado |
|---|---|---|---|
| Movimiento con exotraje | Correr, doble salto, dash, slide y stomp. | Combate (daño de dash y stomp) | Implementado |
| Armas e inventario | Diez armas, dos ranuras, recarga, apuntado y munición. | Economía | Implementado |
| IA de mutantes | Aparición, persecución, ataque, salto y glitch de los científicos. | Rondas, zonas | Implementado |
| Rondas | Cantidad, vida y velocidad de los mutantes por ronda. | IA de mutantes | Implementado |
| Economía | Ganar y gastar puntos. | Combate, rondas | Implementado |
| Zonas y puertas | Abrir zonas y decidir dónde aparecen los mutantes. | Economía | Implementado |
| Impresora 3D | Arma al azar por 950 puntos. | Economía, armas | Implementado |
| Mejoras de arma | Niveles MK1 a MK4 del arma en mano. | Economía, armas | Implementado |
| Pilas de Tannat | Siete mejoras permanentes para la partida. | Economía, vida, armas, movimiento | Implementado |
| Power-ups | Drops temporales o instantáneos. | IA de mutantes, economía | Implementado |
| Trampas | Matan mutantes en un área por un tiempo. | Economía | Implementado |
| Estilo | Medidor y rangos de D a S. | Combate | Implementado |
| Interruptor de energía | Objetivo a mitad de partida que enciende estaciones y trampas. | Zonas | Planeado |
| Rondas especiales y científico EMZ | Romper la rutina cada 4 o 5 rondas y contrarrestar el exotraje. | Rondas, IA | Planeado |

## Sistemas

### Sistema de IA de mutantes

**Objetivo:**  
Hacer que los mutantes localicen y persigan al jugador de forma constante, reforzando la tensión psicológica del juego.

**Entradas:**  
Posición del jugador, punto de aparición del mutante, número de ronda.

**Procesamiento / reglas:**  
Cada mutante sale del suelo, se dirige hacia Tannat y lo sigue. Al entrar en rango (1.7 m) ataca cuerpo a cuerpo (40 de daño, una vez por segundo). Desde la ronda 3 algunos saltan hacia Tannat (de 3 a 9 m, 30 de daño); desde la ronda 3 aparecen corredores, y desde la ronda 10 todos corren. Si un mutante pasa 30 s sin contacto (o 10 s a más de 40 m), sin daño y fuera de la vista, desaparece y vuelve a aparecer cerca del jugador. Un mutante que no puede navegar durante 10 s vuelve a su punto de aparición.

**Salidas:**  
Movimiento hacia el jugador; ataque al alcanzarlo; efecto de glitch (picos, remolino y destellos invertidos).

**Estados posibles:**  
Saliendo del suelo, persiguiendo, saltando, atacando, eliminado.

**Dependencias:**  
El sistema de rondas determina la cantidad y la vida; el de zonas decide qué puntos de aparición están activos.

**Interacciones:**  
Con el combate del jugador y con la economía (cada baja otorga puntos y puede soltar un power-up).

**Datos que necesita:**  
Posición de Tannat, puntos de aparición activos y los valores de `ZombieSettings` y `RoundSettings`.

**Datos que genera:**  
Eventos de muerte (puntos, estilo, power-ups) y de daño al jugador.

**Riesgos:**  
Atascos en esquinas o rampas y pérdida de rendimiento con muchos enemigos.

**Criterios de aceptación:**  
Los mutantes recorren todas las zonas abiertas sin atravesar obstáculos, atacan dentro del rango previsto y registran su muerte una sola vez.

### Sistema de armas e inventario

El jugador inicia con la pistola. Al comprar un arma se ocupa la ranura libre; si las dos están llenas, se sustituye la que está en la mano. El sistema controla disparo, apuntado, recarga, cambio de arma y munición, y actualiza el HUD. Cada arma conserva su cargador, su reserva y su nivel de mejora.

### Sistema de rondas

Las primeras cinco rondas tienen 6, 8, 13, 18 y 24 mutantes; después la cantidad crece con la ronda. Nunca hay más de 32 vivos a la vez. La vida empieza en 150 y sube 100 por ronda hasta la ronda 9; después se multiplica por 1.1 cada ronda. La velocidad sube 0.3 por ronda hasta 9 m/s. Entre rondas hay 10 s de descanso. La ronda espera solo a los mutantes que ella generó.

### Sistema de economía

Ver [[06 - Economía y Recursos]].

### Sistema de zonas y puertas

Al comenzar, solo está abierta la Sala de Contención. Cada puerta comunica dos zonas y se paga una vez. Los mutantes aparecen solo en zonas abiertas: en la zona donde está Tannat y en las zonas conectadas a ella por puertas. Así, moverse por el mapa cambia de dónde viene la horda.

### Impresora 3D

Cuesta 950 puntos e imprime un arma al azar que el jugador no lleva (incluido el cohete, que no está en ninguna pared). Hay que tomarla con E antes de que expire. Si la impresión falla, devuelve los puntos y la impresora se mueve a otra de sus cinco ubicaciones.

### Mejoras de arma

Las estaciones mejoran el arma en mano un nivel, la recargan y multiplican su daño:

| Nivel | Costo | Daño |
|---|---:|---:|
| MK1 | 3,000 | ×1.5 |
| MK2 | 4,500 | ×2 |
| MK3 | 6,000 | ×2.75 |
| MK4 (solo estación experimental) | 7,500 | ×3.75 |

La estación experimental del hangar está bloqueada hasta tomar la llave del incinerador.

### Pilas de Tannat

Tannat tiene cuatro espacios. Cada pila cuesta 2,000 más 500 por cada pila ya instalada, salvo RESPALDO, que cuesta siempre 500 y se puede instalar tres veces por partida.

| Pila | Efecto |
|---|---|
| BLINDAJE | Vida máxima de 160 (aguantas un golpe más). |
| RÁFAGA | Disparas 25 % más rápido. |
| SERVO | Recargas 30 % más rápido. |
| PISTÓN | Corres más; slide y stomp vuelven antes. |
| RESPALDO | Si caes, te reinicia (3 s); se pierde junto con la última pila instalada. |
| FILTRO | La vida vuelve antes y más rápido. |
| DESCARGA | Al recargar sueltas una descarga (de 150 a 600 de daño, de 1 a 4 m; más fuerte cuanto más vacío estaba el cargador). |

### Power-ups

Cada baja tiene 3 % de probabilidad de soltar uno (máximo 4 por ronda), y además hay uno garantizado cada cierta cantidad de puntos ganados (2,000 al inicio, creciendo ×1.14). El drop dura 30 s en el suelo y parpadea al final. Los efectos con duración duran 30 s.

| Power-up | Efecto |
|---|---|
| PUNTOS DOBLES | Los puntos valen el doble. |
| LETAL | Cualquier impacto mata. |
| PURGA | Mata a todos los mutantes vivos y da 400 puntos. |
| MUNICIÓN MÁXIMA | Llena la munición. |
| IMPULSO | Saltas más alto, corres más y tienes un salto aéreo extra. |

### Trampas

Cuestan 1,000 puntos: durante 20 s matan a todo mutante que pise su área, sin dar puntos ni estilo; al terminar se recargan durante 40 s antes de poder comprarse otra vez. Hay dos: la descontaminación de Administración y el anillo eléctrico del Laboratorio Central.

### Arnés del exotraje

En el hangar de Pruebas Exo, por 1,500 puntos y una vez por partida: un salto aéreo extra, un poco más de velocidad y altura de salto, y enfriamientos más cortos.

### Estilo

Dañar y eliminar llena el medidor; se gana más con bajas en el aire, en slide, rápidas, en movimiento, en cadena y con disparos a la cabeza. Se vacía con el tiempo (más rápido si Tannat está quieto) y al recibir daño. Cada 100 de estilo se sube un rango (D, C, B, A, S), y cada rango multiplica los puntos ganados (D ×1, C ×1.25, B ×1.5, A ×2, S ×2.5). La pantalla de resultados muestra el mejor rango.

## Relaciones entre sistemas

La aparición usa solo las zonas abiertas cercanas a Tannat. La IA conduce a los mutantes hasta él y comunica sus bajas a rondas, economía, estilo y power-ups. Los puntos compran armas, puertas, mejoras, pilas, trampas y el arnés; las pilas y las mejoras modifican el combate y el movimiento.

> **Navegación:** [[00 - Índice]] · ← [[02 - Mecánicas]] · [[04 - Controles]] →
