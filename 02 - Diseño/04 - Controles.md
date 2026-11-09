# Controles

## Descripción de la sección

Define la relación entre las acciones del jugador y las entradas físicas del dispositivo.

## Mapa de controles

| Acción | Teclado y mouse | Mando |
|---|---|---|
| Mover / mirar | W, A, S, D / mouse | Stick izquierdo / stick derecho |
| Saltar (y doble salto en el aire) | Espacio | A (botón inferior) |
| Dash | Shift izquierdo | LB |
| Slide (en el suelo) / stomp (en el aire) | Ctrl izquierdo o C | B para slide, RB para stomp |
| Apuntar / disparar | Clic derecho / clic izquierdo | LT / RT |
| Recargar | R | X (botón izquierdo) |
| Interactuar / comprar | E | X (botón izquierdo) |
| Cambiar de arma | 1, 2 o rueda del mouse | Y (botón superior) |
| Soltar arma | G | Cruceta abajo |
| Pausa | Esc | Start |
| Volver al menú (en pausa o al terminar) | Q | Select |
| Reiniciar el nivel (al terminar) | R | A (botón inferior) |

**Controles adicionales:** los enlaces viven en `Assets/_Game/Input/PlayerControls.inputactions` (Input System de Unity). No hay controles táctiles.

## Principios de control

- Los controles deben ser consistentes.
- Las acciones críticas deben ser fáciles de identificar.
- Debe existir retroalimentación visual, sonora o háptica cuando corresponda.
- Evitar combinaciones innecesariamente complejas.

## Reasignación

¿El jugador puede cambiar los controles?

No en esta versión: el esquema es fijo. Los ajustes permiten cambiar la sensibilidad y el campo de visión (ver [[04 - Guardado y Configuración]]).

## Entrada y retroalimentación

Describe qué ocurre inmediatamente después de cada entrada importante.

Al disparar se muestran el retroceso, el fogonazo, el trazador y el impacto, con el sonido del arma; al apuntar desaparece la mira central (el rifle de tirador muestra su mira telescópica). El dash y el stomp tienen efectos en el HUD y en la cámara. Al comprar, se actualizan los puntos y se entrega la compra; si faltan puntos aparece "Puntos insuficientes". Las bajas en cadena reproducen un sonido de combo.

> **Navegación:** [[00 - Índice]] · ← [[03 - Sistemas]] · [[05 - Progresión]] →
