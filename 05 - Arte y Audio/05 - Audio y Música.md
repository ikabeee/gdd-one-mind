# Audio y Música

## Descripción de la sección

Define la identidad sonora y cómo el audio comunica información al jugador.

## Música

**Tema del menú:** «coso carlos», aportado por el dueño (etiquetas: artista anthonyux98, «made with suno»). Dura 193 s. Empieza en la frase elegida («La B», hacia los 0:27), con una intro de 18.22 s una vez y un bucle de 106.3 s; objetivo −19.0 LUFS; se atenúa al lanzar la partida. El archivo no declara licencia.

**En la partida:** no hay música.

> [!warning] Recortado para la entrega (2026-11-12)
> La partida no tiene música de combate ni de transición entre rondas. Ver [[05 - Gestión de Cambios]].

## Efectos de sonido

| Evento | Sonido | Propósito |
|---|---|---|
| Disparo | Un clip por arma para 9 de las 10 (el Cohete no tiene); paquetes Sonniss GDC, más la biblioteca Free Firearm Sound en las escopetas. Sin archivo CREDITS. | Confirmar el disparo junto con el fogonazo y el retroceso. |
| Recarga y cambio de arma | Golpes por arma (cargador fuera, cargador dentro, cerrojo, cartucho, ...), sincronizados con las animaciones; Freesound, CC0 1.0 por clip. | Confirmar la acción sin mirar el HUD. |
| Cargador vacío | Clic de arma vacía. | Avisar que hay que recargar. |
| Pasos | Tannat en concreto y metal (6 cada uno) y aterrizajes; mutantes en concreto y metal; 29 clips. Freesound, CC0 1.0 por clip. | Marcar el movimiento propio y el de la horda. |
| Movimiento | Capas de aterrizaje y de stomp (contacto, golpe, crujido, servo, ...); 32 clips, más capas sintetizadas. Freesound, CC0 1.0, más sintetizado. | Reforzar aterrizajes y stomps. |
| Ambiente | Base por zona con fundido de 2 s, 12 sonidos lejanos cada 2 a 8 s, emisores cercanos y murmullo de horda con las voces del juego; 30 clips. Freesound, CC0 1.0 por grabación. | Dar aire al laboratorio. |
| Mutante aparece / ataca / muere | 8 llamadas en 3 niveles (cuerdo, loco, lleno); 26 clips por nivel, 78 en total. CC0 de tonsil5 (Freesound) con tono bajado, sobre gruñidos Glitchedtones. Sin archivo CREDITS. | Ubicar a los mutantes y confirmar bajas. |
| Combo de bajas | 8 aguijones (uno por eslabón, un tono más alto) y una resolución; atenúan el juego 1.5 dB por baja, hasta 9 dB. Sintetizados por herramienta. | Marcar la racha sin mirar el HUD. |
| Daño a Tannat | Impacto metálico. | Avisar que se recibe daño. |

Sin sonido en la entrega: vidrio que se rompe, compra y rechazo en máquinas, puertas, inicios y fines de ronda, y locución.

## Audio espacial

¿Se utilizará audio posicional?

Sí, para los mutantes: permite saber por dónde se acercan y refuerza el pilar de tensión constante. *(propuesta)*

## Voz

**Narración:** No hay narración.

**Diálogos hablados:** No hay diálogos hablados. Las voces de los infectados no son verbales: 8 llamadas en 3 niveles de locura.

**Idiomas:** No aplica (no hay voz).

## Mezcla

Define prioridades, volumen relativo y comportamiento de la música ante eventos importantes.

Prioridad: sonidos de peligro (mutantes, daño) > armas > interfaz > música. El combo de bajas atenúa el juego 1.5 dB por baja, hasta 9 dB. La música del menú se atenúa al lanzar la partida.


> **Navegación:** [[00 - Índice]] · ← [[04 - Interfaz Visual]] · [[06 - Galería de Arte]] →
