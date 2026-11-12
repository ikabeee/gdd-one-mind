# Criterios de Calidad

## Descripción de la sección

Define qué significa que una característica esté correctamente terminada.

## Calidad funcional

- [ ] Funciona según las reglas documentadas.
- [ ] No produce errores conocidos críticos.
- [ ] Maneja casos límite importantes (ver casos especiales en [[07 - Reglas y Estados del Juego]]).

## Calidad de experiencia

- [ ] El jugador entiende el objetivo: sobrevivir el mayor número de rondas.
- [ ] Las respuestas del juego son claras: disparo, impacto, compra y rechazo tienen respuesta visual y sonora.
- [ ] La dificultad es coherente: aumenta con cada ronda.
- [ ] La interfaz es comprensible: vida, munición, puntos y costos se leen de un vistazo.

## Calidad técnica

- [ ] Rendimiento aceptable: 60 FPS en equipos de gama media.
- [ ] Sin errores críticos.
- [ ] Guardado estable: no aplica, no hay guardado de partida.
- [ ] No existen dependencias rotas.

## Definición de terminado

Una característica se considera terminada cuando:

- Cumple las reglas descritas en el GDD.
- Cumple sus [[04 - Criterios de Aceptación]].
- Fue probada en la versión jugable para Windows, no solo dentro de Unity.
- Tiene su respuesta visual y sonora, si la requiere.
- No introduce errores bloqueantes ni baja el rendimiento por debajo del objetivo.
- Otro integrante del equipo la revisó.

## Pendiente de verificar en la entrega (2026-11-12)

- 60 FPS en equipos de gama media (medición solo en editor por lotes; el dueño reporta problemas tras la ronda 1).
- Builds de macOS y Windows en máquina real (Windows sin ejecutar; sin partida completa jugada).
- Respuesta sonora de compra, denegación, puertas y rondas (sin implementar).
- Audio escuchado en juego (menú, pasos, ambiente, murmullo).


> **Navegación:** [[00 - Índice]] · ← [[05 - Gestión de Cambios]] · [[02 - Pruebas]] →
