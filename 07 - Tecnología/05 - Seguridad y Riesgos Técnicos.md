# Seguridad y Riesgos Técnicos

## Descripción de la sección

Documenta riesgos técnicos y medidas para reducir fallos, pérdida de datos o abuso de sistemas.

## Riesgos

| Riesgo | Probabilidad | Impacto | Mitigación |
|---|---|---|---|
| Mutantes atascados o rezagados que impiden terminar la ronda. | Media | La ronda no termina. | Implementado: un mutante sin poder navegar 10 s vuelve a su punto de aparición; los rezagados (30 s sin contacto, o 10 s a más de 40 m) reaparecen cerca del jugador; la ronda espera solo a los mutantes que generó. |
| Tannat queda atascado o sale del mapa. | Media | Rompe el movimiento y frustra al jugador. | Implementado: si sale del área jugable reaparece dentro; un stomp atorado en pendiente termina solo. |
| Un mutante no registra su muerte o la registra dos veces. | Baja | La ronda no termina o se otorgan puntos de más. | Cubierto por pruebas unitarias y de flujo completo. |
| Valores que crecen sin límite en rondas altas. | Baja | Vida o cantidad de mutantes infinitas. | Implementado: la vida tiene tope de 2^24 y la cantidad de mutantes por ronda siempre es finita. |
| Explosiones que lanzan a Tannat sin control. | Baja | Movimiento roto. | Implementado: un empuje por salto, con tope de 45 m/s. |
| Rendimiento por debajo de 60 FPS en los equipos del showcase. | Media | Mala experiencia en la presentación. | Tope de 32 mutantes vivos; falta medir en una build de Windows en equipos similares. |
| Economía desbalanceada. | Media | Rondas demasiado fáciles o imposibles. | Ajustar costos y puntos con playtests. |
| El maestro intenta "romper el juego" una semana antes de la entrega. | Alta | Errores visibles en la evaluación. | Ronda de pruebas "break the game" ya hecha y corregida; seguir agregando pruebas por cada error encontrado. |

## Datos sensibles

El diseño actual es para un jugador y no requiere conexión. No se han definido cuentas ni recolección de datos personales.

## Multijugador

No aplica al alcance actual: el juego es para un jugador y funciona sin conexión.

Autenticación, autoridad de servidor y comunicación multijugador: no aplican a esta versión.

## Recuperación

¿Qué ocurre ante corrupción de datos, pérdida de conexión o fallo del programa?

No hay datos guardados ni conexión que proteger. Si el programa falla, se pierde la partida en curso, lo que es coherente con el diseño: el progreso nunca se conserva.


> **Navegación:** [[00 - Índice]] · ← [[04 - Datos y Persistencia]] · [[01 - Alcance]] →
