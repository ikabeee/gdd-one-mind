# UI y Menús

## Descripción de la sección

Define la estructura funcional de las interfaces y menús.

## Mapa de navegación

```text
Menú principal
├── Jugar (entra directo a BROTE)
├── Ajustes
└── Salir (con confirmación)

Durante la partida
└── Pausa
    ├── Continuar
    ├── Reiniciar partida
    ├── Ajustes
    ├── Controles
    ├── Menú principal
    └── Salir del juego (con confirmación)

Después de la derrota
├── Reintentar (R o X / botón sur; comienza una nueva partida)
└── Volver al menú (Q o Select)
```

«Jugar» entra directo a BROTE, sin pantalla de nivel. No hay opción de continuar una partida guardada.

## Pantallas

### Pantallas de la partida

**Propósito:**  
Iniciar el juego, ajustar opciones, consultar controles, pausar y conocer el resultado al terminar.

**Elementos:**  
Menú principal, HUD, menú de pausa (con páginas de ajustes y controles) y pantalla de derrota.

**Acciones disponibles:**  
Jugar, ajustar, consultar controles, salir, reanudar, reiniciar y volver al menú, según la pantalla.

**Estados:**  
Menú, inicio, combate, transición entre rondas, pausa y derrota.

**Transiciones:**  
Jugar entra directo en la Zona 1 de BROTE. Pausa permite reanudar o abandonar la sesión. Al reintentar tras la derrota se reinicia el estado de la partida.

### Menú principal

Título «ONE MIND» sobre un diorama 3D: Cuyus trepa a Tannat en bucle. Opciones: JUGAR («ENTRAR AL BROTE»), AJUSTES («SENSIBILIDAD, CAMPO DE VISION Y VOLUMEN») y SALIR («CERRAR ONE MIND», con confirmación «SALIR DE ONE MIND?» / «SI, SALIR» / «NO»). Etiqueta de esquina «+ ONEMIND_01 / VER. 0.1_PROTO». Al elegir Jugar, un avance de 0.8 s lleva directo a BROTE.

### HUD en partida

Muestra: contador de ronda (parpadea al empezar), «RESTANTES», puntos, multiplicador y placa de rango de estilo, munición, icono del arma activa y dos casillas de arma, casillas de dash y stomp, bloque de estado (UNIDAD / SISTEMAS), retrato de Cuyus con la bahía de pilas, iconos de los power-ups temporales, cruz fina (oculta al apuntar), mira telescópica del Rifle de tirador y efectos de daño y glitch. Los avisos de interacción aparecen con E y su precio; si faltan puntos, el precio se hincha en rojo y escribe «Faltan N». Los power-ups temporales aparecen solo como iconos; PURGA y MUNICION MAXIMA muestran su mensaje durante 2.5 s.

> [!warning] Recortado para la entrega (2026-11-12)
> El HUD perdió sus textos extra para la entrega: nombre del arma, avisos de recarga e inicio de ronda, «Siguiente ronda en N», nombres y tiempos de los power-ups, ayudas de controles y de la impresora, y el filtro CRT. Ver [[05 - Gestión de Cambios]].

### Menú de pausa

«PAUSA»: CONTINUAR, REINICIAR PARTIDA, AJUSTES, CONTROLES (columnas de teclado y de mando), MENU PRINCIPAL y SALIR DEL JUEGO, con confirmaciones SI / NO. El audio se pausa con el juego. Funciona con teclado, mouse y mando.

### Pantalla de derrota

Título «GAME OVER» con las rondas sobrevividas («Sobreviviste N rondas»). Desde 1.1 s se puede saltar (reintentar o ir al menú); después de una caída a negro muestra a Tannat arrodillado apagándose y unas tomas del mapa, y vuelve al menú principal si no hay entrada.

## Confirmaciones

Reiniciar o salir al menú pide confirmación con SI / NO. Ambas acciones interrumpen la partida y avisan de que el progreso se pierde.


> **Navegación:** [[00 - Índice]] · ← [[01 - UX y Flujo del Jugador]] · [[03 - Accesibilidad]] →
