# Audio y Música

## Descripción de la sección

Define la identidad sonora y cómo el audio comunica información al jugador.

## Música

> [!warning] Estado (2026-11-09)
> El juego todavía no tiene música: el mezclador ya tiene el canal y el volumen de música se puede ajustar en Ajustes, pero faltan las pistas. Lo siguiente sigue siendo propuesta.

*(propuesta)*

**Estilo:** Ambiental oscura y tensa, con elementos electrónicos.

**Instrumentación:** Sintetizadores, percusión electrónica y sonidos industriales.

**Temas principales:** Menú principal, combate y transición entre rondas.

**Música dinámica:** Sí. Sube de intensidad durante el combate y baja en la transición entre rondas.

## Efectos de sonido

Hoy solo los disparos, el combo y la navegación del menú principal tienen sonido en el juego; los demás eventos de la tabla están pendientes.

| Evento | Sonido | Propósito |
|---|---|---|
| Disparo | Un sonido propio por arma (las ocho armas de pared y la pistola; falta el cohete). Implementado. | Confirmar el disparo junto con el fogonazo y el retroceso. |
| Combo de bajas | Ocho notas armonizadas que suben con cada baja en cadena y una resolución final; baja el volumen del resto del juego mientras suena. Implementado. | Premiar las bajas encadenadas. |
| Navegación del menú principal | Tic corto generado por código al cambiar de opción. Implementado. | Confirmar el cambio de selección. |
| Compra válida / puntos insuficientes | Confirmación o rechazo; archivos pendientes. | Distinguir si se realizó la compra o faltan puntos. |
| Recarga y cambio de arma | Sonido mecánico por arma. | Confirmar la acción sin mirar el HUD. |
| Cargador vacío | Clic de arma vacía. | Avisar que hay que recargar. |
| Mutante aparece / ataca / muere | Gruñidos y golpes. | Ubicar a los mutantes y confirmar bajas. |
| Daño a Tannat | Impacto metálico. | Avisar que se recibe daño. |
| Apertura de la puerta | Sonido de puerta de seguridad. | Confirmar el acceso a una zona nueva. |
| Inicio de ronda | Señal o alarma corta. | Marcar el fin del descanso. |

## Audio espacial

¿Se utilizará audio posicional?

Sí, para los mutantes: permite saber por dónde se acercan y refuerza el pilar de tensión constante. *(propuesta)*

## Voz

**Narración:** No hay narración.

**Diálogos hablados:** No hay diálogos hablados.

**Idiomas:** No aplica (no hay voz).

## Mezcla

Define prioridades, volumen relativo y comportamiento de la música ante eventos importantes.

Prioridad *(propuesta)*: sonidos de peligro (mutantes, daño) > armas > interfaz > música. La música baja de volumen cuando hay muchos efectos simultáneos.


> **Navegación:** [[00 - Índice]] · ← [[04 - Interfaz Visual]] · [[01 - UX y Flujo del Jugador]] →
