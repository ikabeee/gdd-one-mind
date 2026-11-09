# Economía y Recursos

## Descripción de la sección

Documenta cualquier recurso cuantificable: dinero, vida, energía, munición, experiencia, materiales, tiempo, puntos, etc.

## Recursos

- **Puntos:** se empieza con 500. Se ganan al dañar y eliminar mutantes y se gastan en armas, munición, puertas, trampas, mejoras y pilas. Se pierden al terminar la partida.
- **Munición:** cada arma tiene cargador y reserva propios. Se repone con la compra de pared del arma, con cada mejora MK o con el power-up MUNICIÓN.
- **Vida:** 100 (160 con la pila BLINDAJE). Se regenera sola tras 2.5 s sin daño, a 60 por segundo. No hay compra de armadura ni de vida. Caer sin RESPALDO termina la partida.

## Fuentes y sumideros

**Fuentes:** formas en las que el jugador obtiene recursos.

| Acción | Puntos |
|---|---:|
| Impacto que no mata | 10 |
| Baja al cuerpo | 60 |
| Baja con disparo a la cabeza | 100 |
| Baja con stomp o dash | 130 |
| Baja con trampa o con PURGA | 0 |
| Power-up PURGA | 400 fijos |

El **rango de estilo** multiplica los puntos ganados: D ×1, C ×1.25, B ×1.5, A ×2 y S ×2.5. El power-up PUNTOS DOBLES los duplica. Los mutantes también pueden soltar power-ups al morir (ver [[04 - Objetos y Coleccionables]]).

**Sumideros:** formas en las que el jugador los gasta.

| Compra | Costo |
|---|---:|
| Armas de pared | 500 – 2,000 |
| Munición | Ver [[#Recarga de munición]] |
| Puertas | 750 – 1,250 |
| Trampas | 1,000 |
| Ducto al Incinerador | 500 |
| Impresora 3D | 950 |
| Arnés Exo | 1,500 |
| Estación de mejora | MK1 3,000 · MK2 4,500 · MK3 6,000 · MK4 7,500 |
| Pilas | 2,000 + 500 por pila instalada; RESPALDO 500 |

Precios por arma en [[04 - Objetos y Coleccionables]] y por puerta en [[02 - Niveles]].

### Recarga de munición

Para reponer la munición se usa otra vez la compra de pared de un arma que ya se tiene y que no está llena.

**Precio = costo de munición × (nivel de mejora del arma + 1).** El costo de munición es la mitad del precio del arma.

| Arma | Precio del arma | Costo de munición |
|---|---:|---:|
| Pistola | 0 | 0 |
| Rifle | 500 | 250 |
| Escopeta | 500 | 250 |
| Blaster | 750 | 375 |
| Rifle de asalto | 1,000 | 500 |
| Subfusil | 1,250 | 625 |
| Escopeta de bomba | 1,250 | 625 |
| Rifle de tirador | 1,500 | 750 |
| Ametralladora | 2,000 | 1,000 |
| Cohete | Solo en la impresora 3D | 750 |

| Nivel del arma | Multiplicador |
|---|---:|
| Sin mejorar | ×1 |
| MK1 | ×2 |
| MK2 | ×3 |
| MK3 | ×4 |
| MK4 | ×5 |

Ejemplo: reponer la Ametralladora con MK2 cuesta 1,000 × 3 = 3,000. El Cohete no tiene compra de pared; su munición se repone con una mejora MK o con el power-up MUNICIÓN.

## Reglas

Define límites, regeneración, acumulación, intercambio y condiciones especiales.

- Los puntos no tienen límite de acumulación y no se regeneran solos.
- No se pueden vender ni intercambiar armas.
- Cada puerta se cobra una sola vez por partida.
- Cada arma tiene cargador y reserva propios e independientes.
- La vida se regenera sola tras 2.5 s sin daño; no se puede comprar.
- Las bajas con trampa o con PURGA no dan puntos.
- Al terminar la partida se pierden puntos, armas, mejoras, pilas y las puertas abiertas.

## Balance

### Balance económico inicial

Los valores de esta nota son los del juego en Unity y siguen sujetos a playtests. Tannat empieza con 500 puntos: alcanzan para el Rifle o la Escopeta de la Sala de Contención, pero no para la primera puerta (750). Una baja al cuerpo da 60 puntos y una con stomp o dash, 130; el rango de estilo multiplica todo lo ganado hasta ×2.5.

¿Qué comportamiento queremos incentivar?

Tomar decisiones de compra activas, abrir nuevas zonas para ganar espacio de maniobra y moverse constantemente.

¿Qué comportamiento queremos evitar?

Quedarse quieto en una esquina, acumular puntos sin gastarlos nunca, y que la munición sobre tanto que comprarla no importe o falte tanto que resulte frustrante.


> **Navegación:** [[00 - Índice]] · ← [[05 - Progresión]] · [[07 - Reglas y Estados del Juego]] →
