# Objetos y Coleccionables

## Descripción de la sección

Define objetos que el jugador puede recoger, utilizar, equipar, vender, intercambiar o descubrir.

## Catálogo de armamento

**Tipo:** Armas equipables (máximo dos a la vez).

**Cómo se utiliza:** clic izquierdo para disparar, clic derecho para apuntar, R para recargar, 1/2 o rueda del mouse para cambiar, G para soltar.

**Restricciones:** se necesita munición para disparar y puntos para comprar. Con ambas ranuras ocupadas, una compra reemplaza el arma en la mano.

**Representación visual:** modelos 3D low poly con miras de hierro detalladas; el rifle de tirador usa mira telescópica. Fogonazo, trazadores e impactos planos (flipbooks).

| Arma | Disparo | Daño | Disparos/s | Cargador / reserva | Dónde se obtiene | Costo (munición) |
|---|---|---:|---:|---|---|---:|
| Pistola | Semiautomática | 40 | 6 | 8 / 64 | Inicial | Gratis |
| Rifle | Semiautomático | 100 | 5 | 8 / 96 | Pared, Sala de Contención | 500 (250) |
| Escopeta | 8 perdigones | 25 c/u | 1.4 | 6 / 36 | Pared, Sala de Contención | 500 (250) |
| Blaster | Semiautomático | 70 | 4 | 10 / 80 | Pared, Administración | 750 (375) |
| Subfusil | Automático | 28 | 15 | 32 / 192 | Pared, Administración | 1,250 (625) |
| Rifle de asalto | Automático | 35 | 11 | 30 / 150 | Pared, Laboratorio Central | 1,000 (500) |
| Escopeta de bomba | 9 perdigones | 30 c/u | 1.1 | 8 / 48 | Pared, Morgue | 1,250 (625) |
| Ametralladora | Automática | 45 | 12 | 100 / 300 | Pared, Celdas | 2,000 (1,000) |
| Rifle de tirador | Semiautomático, mira telescópica | 160 | 3 | 10 / 60 | Pared, Pruebas Exo | 1,500 (750) |
| Cohete | Proyectil con explosión (400) | 100 | 1.2 | 4 / 24 | Solo impresora 3D | 950 por impresión |

Todas las armas pueden pasar por la impresora 3D. Las mejoras MK1 a MK4 multiplican el daño (ver [[03 - Sistemas]]).

## Power-ups

**Tipo:** Drops de los mutantes; se recogen pasando sobre ellos.

| Power-up | Efecto | Duración |
|---|---|---|
| PUNTOS DOBLES (x2) | Los puntos valen el doble. | 30 s |
| LETAL | Cualquier impacto mata. | 30 s |
| PURGA | Mata a todos los mutantes vivos y da 400 puntos. | Instantáneo |
| MUNICIÓN MÁXIMA | Llena la munición. | Instantáneo |
| IMPULSO | Saltas más alto, corres más y tienes un salto aéreo extra. | 30 s |

El drop permanece 30 s en el suelo y parpadea en los últimos 12 s.

## Pilas de Tannat

**Tipo:** Mejoras permanentes para la partida, instaladas en estaciones de carga (una por pila, repartidas por las zonas).

| Pila | Efecto | Estación |
|---|---|---|
| FILTRO | La vida vuelve antes y más rápido. | Sala de Contención |
| RESPALDO | Si caes, te reinicia (3 por partida). | Administración |
| DESCARGA | Al recargar sueltas una descarga. | Administración |
| RÁFAGA | Disparas 25 % más rápido. | Laboratorio Central |
| SERVO | Recargas 30 % más rápido. | Morgue |
| BLINDAJE | Vida máxima de 160. | Celdas |
| PISTÓN | Corres más; slide y stomp vuelven antes. | Pruebas Exo |

**Valor:** 2,000 + 500 por pila ya instalada; RESPALDO cuesta 500. **Cantidad máxima:** 4 pilas.

**Representación visual:** cada pila tiene un color y un ícono de 7×7 píxeles en el HUD, para distinguirlas también sin color.

## Objetos del mapa

| Objeto | Función | Costo |
|---|---|---:|
| Impresora 3D | Arma al azar; cambia de lugar entre 5 ubicaciones. | 950 |
| Estación de mejora (Administración, Celdas) | MK1 a MK3 del arma en mano. | 3,000 a 6,000 |
| Estación experimental (Pruebas Exo) | MK4; bloqueada hasta tener la llave. | 7,500 |
| Trampa de descontaminación (Administración) | Mata mutantes en su área durante 20 s; después se recarga durante 40 s. | 1,000 |
| Anillo eléctrico (Laboratorio Central) | Mata mutantes en su área durante 20 s; después se recarga durante 40 s. | 1,000 |
| Orbes de dash (6 en el Laboratorio Central, 3 en Pruebas Exo) | Al tocarlos se recuperan el dash, los saltos aéreos y el stomp; reaparecen a los 2 s. | — |
| Arnés del exotraje (Pruebas Exo) | Salto aéreo extra, más velocidad y enfriamientos cortos. | 1,500 |
| Conductos (Administración, Pruebas Exo) | Bajan al incinerador. | 500 |
| Llave del incinerador | Desbloquea la estación experimental. | — |
| Interruptor de pisotón (Celdas) | Un stomp fuerte suelta un power-up al azar. | — |

> [!note] Mejoras retiradas
> Las mejoras "abastecer munición", "armadura" y "restablecer vida" de la versión 0.3 se reemplazaron por las pilas (BLINDAJE, FILTRO), la regeneración de vida y el power-up MUNICIÓN MÁXIMA.

> **Navegación:** [[00 - Índice]] · ← [[03 - Enemigos y NPC]] · [[05 - Misiones y Desafíos]] →
