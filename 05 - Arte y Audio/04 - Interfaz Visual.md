# Interfaz Visual

## Descripción de la sección

Documenta la información que el juego muestra al jugador y las reglas visuales de la interfaz.

## HUD

El HUD muestra: contador de ronda (parpadea al empezar), «RESTANTES» (mutantes que quedan), puntos, multiplicador y placa de rango de estilo, munición, icono del arma activa y dos ranuras de arma, iconos de dash y stomp, bloque de estado (UNIDAD / SISTEMAS, señal y porcentaje), retrato de Cuyus con la bahía de pilas, iconos de power-ups con duración, mira fina (se oculta al apuntar), visor del Rifle de tirador, y efectos de glitch de daño y de ronda.

- **Vida:** bloque de estado de Tannat (UNIDAD / SISTEMAS).
- **Energía:** no hay barra; el movimiento no consume estamina.
- **Munición:** munición del arma equipada; «SIN MUNICION» y «R recargar» con un cuarto de cargador.
- **Objetivo:** ronda actual y «RESTANTES».
- **Mapa:** no hay minimapa ni pantalla de mapa.
- **Recursos:** puntos disponibles.
- **Indicadores contextuales:** costo y tecla E al acercarse a una compra («E comprar <arma> [precio]», «E municion <arma> [precio]», «E abrir <zona> [precio]», «E imprimir arma [950]», «E tomar <arma>», «E activar trampa [1000]», «trampa activa», «trampa recargando», avisos de instalación de pilas, «sin energia»).

## Jerarquía visual

Retrato y bahía arriba a la izquierda; dash y stomp a la izquierda; ronda abajo a la izquierda; iconos de power-ups con duración sobre «RESTANTES» abajo al centro; puntos y rango de estilo a la derecha; arma, munición y ranuras abajo a la derecha.

Prioridad:

1. Vida de Tannat y munición del arma equipada.
2. Puntos disponibles y ronda actual.
3. Indicadores contextuales (costo y tecla E).

## Estados

Al disparar se actualiza la munición. Una compra válida descuenta puntos. Si faltan puntos, el costo se agranda en rojo y muestra «Faltan N». Los iconos de power-ups con duración se mantienen fijos y parpadean en los últimos 5 s (más rápido en los últimos 2 s); los instantáneos muestran «PURGA!» o «MUNICION MAXIMA!» durante 2.5 s. Al llegar a cero de vida se muestra la derrota.

## Referencia visual

El HUD es un visor de casco: los módulos laterales giran hacia el centro en perspectiva y el HUD se retrasa un poco respecto a la cámara al moverse. A la izquierda va el retrato: la pantalla de Tannat con la cara de Cuyus, que reacciona y se distorsiona con el daño, y debajo la bahía de pilas. Más imágenes en [[06 - Galería de Arte]].

![[hud-in-game.png]]

## Convenciones

**Tipografía:** Fuente pixel Pixelmix (regular y negrita) con sombra negra dura. No dibuja acentos, así que los textos del juego van sin ellos.

**Paleta:** papel `#F2F2F2`, negro `#0A0A0A` y acento rojo `#D0263F`.

**Iconografía:** Iconos pixel simples y planos (armas, dash, stomp y pilas); la mira es de 1 px.

**Tamaños mínimos:** Texto legible a 1920 × 1080 desde la distancia de juego del showcase.

**Contraste:** Texto claro con contorno o fondo oscuro para leerse sobre cualquier zona del laboratorio.

**Animaciones:** Parpadeo rojo del costo cuando faltan puntos; actualización visible de puntos y munición.

## Pantallas

- **Menú principal:** «ONE MIND» sobre el diorama (Cuyus trepa a Tannat en bucle). Opciones: JUGAR («ENTRAR AL BROTE»), AJUSTES («SENSIBILIDAD, CAMPO DE VISION Y VOLUMEN») y SALIR («CERRAR ONE MIND», con confirmación «SALIR DE ONE MIND?» / «SI, SALIR» / «NO»). Esquina «+ ONEMIND_01 / VER. 0.1_PROTO». JUGAR carga BROTE directamente; no hay pantalla de nivel.
- **Pausa:** «PAUSA» con CONTINUAR, REINICIAR PARTIDA, AJUSTES, CONTROLES (columnas de teclado y mando), MENU PRINCIPAL y SALIR DEL JUEGO, con confirmaciones SI / NO. Funciona con teclado, ratón y mando.
- **Configuración:** cuatro ajustes guardados (sensibilidad, campo de visión, volumen general y volumen de música).
- **Inventario:** dos ranuras de armas; no hay pantalla independiente.
- **Mapa:** no hay pantalla de mapa.
- **Victoria:** no aplica como final del modo endless.
- **Derrota:** «GAME OVER» con las rondas sobrevividas; permite reintentar o volver al menú principal.


> **Navegación:** [[00 - Índice]] · ← [[03 - Entornos]] · [[05 - Audio y Música]] →
