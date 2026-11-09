# Niveles

## Descripción de la sección

Cada nivel debe documentar su propósito jugable, estructura, dificultad, contenido y condiciones de entrada/salida.

## BROTE — Laboratorio de Neuroplex

**Objetivo principal:**  
Sobrevivir al mayor número de rondas mientras Tannat protege a Cuyus en su interior.

**Objetivos secundarios:**  
Reunir puntos, abrir las seis zonas, mejorar armas, instalar pilas y completar la secuencia del incinerador.

**Duración estimada:**  
Entre 5 y 15 minutos como referencia de prueba. La partida puede extenderse mientras el jugador sobreviva.

**Dificultad:**  
Aumenta por ronda (cantidad, vida, velocidad, saltadores y corredores); no depende de la zona.

**Mecánicas introducidas:**  
En la Sala de Contención: movimiento, disparo y compras de pared. Al abrir zonas: impresora 3D, estaciones de mejora, pilas, trampas, arnés y conductos.

**Mecánicas utilizadas:**  
Todas: exotraje, disparo, apuntado, recarga, cambio de arma, compras, power-ups y estilo.

**Enemigos / obstáculos:**  
Científicos infectados que persiguen, saltan y atacan cuerpo a cuerpo. Las puertas limitan el acceso. El mapa tiene pisos superiores, rampas y plataformas altas (hasta 10 m en el Laboratorio Central). En el incinerador, una pared trituradora empuja a Tannat fuera.

**Recompensas:**  
Puntos, power-ups y acceso a armas, mejoras y pilas.

**Puntos de guardado:**  
No hay guardado del avance de una partida.

**Condición de entrada:**  
Elegir BROTE en el menú. Tannat aparece en la Sala de Contención con la pistola, vida completa y 500 puntos.

**Condición de salida:**  
La partida termina al llegar a cero de vida sin RESPALDO. No hay salida del laboratorio.

**Eventos narrativos:**  
Detalles del laboratorio por zona (ver [[02 - Mundo]]). Cuyus no sale del robot.

**Mapa / diagrama:**  
El nivel se diseña en Blender (`ArtSource/Scenes/Outbreak/build_outbreak_blockout.py`) y se exporta como datos (`Outbreak_Level.json`) que Unity convierte en la escena. Las vistas en planta están en `ArtSource/Scenes/Outbreak/renders/`.

### Zonas y conexiones

| Zona | Se abre desde | Costo | Puntos de aparición |
|---|---|---:|---:|
| Sala de Contención | Inicio | — | 6 |
| Administración | Sala de Contención | 750 | 4 |
| Laboratorio Central | Sala de Contención | 1,250 | 4 |
| Morgue | Administración o Laboratorio Central | 1,000 | 4 |
| Celdas | Laboratorio Central | 1,000 | 4 |
| Pruebas Exo | Morgue o Celdas | 1,250 | 5 |
| Incinerador | Conducto (500) desde Administración o Pruebas Exo | 500 | 0 |

## Cuarto de pruebas

**Objetivo principal:**  
Practicar todas las mecánicas en un solo lugar y despejar sus arenas.

**Contenido:**  
Armería gratis (cada arma con munición completa, tantas veces como se quiera), consolas que controlan las rondas (iniciar, saltar el descanso, invocar un mutante, soltar un power-up, sumar puntos, matar a todos), estaciones de pilas, galería de tiro, arena y circuito de movimiento con puntos de control.

**Condición de salida:**  
Despejar la última arena completa el nivel y muestra la pantalla de resultados (tiempo, bajas, puntos y mejor estilo).

## Flujo del nivel

```text
Inicio en la Sala de Contención → Combatir y reunir puntos → Abrir Administración o el Laboratorio Central → Abrir las alas lejanas → Mejorar armas, instalar pilas, bajar al incinerador → Continuar las rondas → Derrota y posibilidad de reintentar
```

## Criterios de calidad

- El objetivo es comprensible.
- Las reglas se pueden aprender.
- El desafío corresponde al nivel de progresión.
- Existe retroalimentación suficiente.
- El jugador entiende por qué tuvo éxito o fracaso.

> **Navegación:** [[00 - Índice]] · ← [[01 - Estructura del Contenido]] · [[03 - Enemigos y NPC]] →
