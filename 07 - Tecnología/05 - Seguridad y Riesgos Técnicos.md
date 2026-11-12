# Seguridad y Riesgos Técnicos

## Descripción de la sección

Documenta riesgos técnicos y medidas para reducir fallos, pérdida de datos o abuso de sistemas.

## Riesgos

| Riesgo | Probabilidad | Impacto | Mitigación |
|---|---|---|---|
| Atascos de mutantes y pérdida de rendimiento al acumularse en la puerta. | Pendiente de pruebas. | Puede impedir el avance de rondas o afectar la fluidez. | Validar recorridos y medir el rendimiento con distintas cantidades de enemigos antes de fijar un límite. |
| Tannat queda atascado en bordes u obstáculos. | Media | Rompe el movimiento y frustra al jugador. | Revisar colisiones del escenario y probar el salto contra bordes. |
| Un mutante no registra su muerte o la registra dos veces. | Media | La ronda no termina o se otorgan puntos de más. | Registrar la muerte una sola vez y probarlo en cada arma. |
| Rendimiento por debajo de 60 FPS en los equipos del showcase. | Media | Mala experiencia en la presentación. | Limitar enemigos activos, reutilizar objetos y probar en equipos similares. Medición en editor por lotes (Rotonda con 32 mutantes): render a GPU de 34.4 ms a 24.5 ms; el dueño reporta problemas tras la ronda 1. |
| Builds sin probar en máquina real (Windows sin ejecutar; macOS 45 s sin ventana; sin partida completa). | Alta | La entrega falla frente al público. | Jugar una partida completa en cada build antes del showcase. |
| Un re-export de Blender reintroduce marcadores ya cortados. | Media | El nivel recupera estaciones, llave, ductos, puestos, orbes y arnés. | El builder rechaza construirlos; mantener el JSON y el builder de acuerdo. |
| Tests en rojo conocidos (4 `ZombieVariantBagTests`, `TheDressingStaysWithinSixtyThousandTriangles`; `ShutdownBodyPlayTests` intermitente). | Media | Regresiones silenciosas tras la entrega. | Corregir o congelar su alcance antes de retomar esas áreas. |
| Economía desbalanceada. | Alta | Rondas demasiado fáciles o imposibles. | Ajustar costos y puntos con playtests. |

## Datos sensibles

El diseño actual es para un jugador y no requiere conexión. No se han definido cuentas ni recolección de datos personales.

## Multijugador

No aplica al alcance actual: el juego es para un jugador y funciona sin conexión.

Autenticación, autoridad de servidor y comunicación multijugador: no aplican a esta versión.

## Recuperación

¿Qué ocurre ante corrupción de datos, pérdida de conexión o fallo del programa?

No hay datos guardados ni conexión que proteger. Si el programa falla, se pierde la partida en curso, lo que es coherente con el diseño: el progreso nunca se conserva.


> **Navegación:** [[00 - Índice]] · ← [[04 - Datos y Persistencia]] · [[01 - Alcance]] →
