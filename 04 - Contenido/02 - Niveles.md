# Niveles

## Descripción de la sección

Cada nivel debe documentar su propósito jugable, estructura, dificultad, contenido y condiciones de entrada/salida.

El juego tiene dos niveles: **BROTE**, el nivel jugable, y **PRUEBAS**, un cuarto de pruebas con todas las mecánicas en un solo sitio. La distribución de zonas, puertas y obstáculos de BROTE está en [[#Zonas de BROTE]].

## BROTE — Laboratorio de Neuroplex

**Objetivo principal:**  
Sobrevivir al mayor número de rondas mientras Tannat protege a Cuyus en su interior.

**Objetivos secundarios:**  
Reunir puntos, conseguir armamento y mejoras, y abrir las puertas hacia las demás zonas para disponer de más espacio.

**Duración estimada:**  
Entre 5 y 15 minutos como referencia de prueba del GDD. La partida puede extenderse mientras el jugador sobreviva.

**Dificultad:**  
Aumenta por ronda mediante la cantidad, la vida y la velocidad de los mutantes (ver [[03 - Enemigos y NPC]]); no depende de la zona.

**Mecánicas introducidas:**  
En la Sala de Contención (Zona 1) se presentan el movimiento, el disparo y las compras en pared. Las puertas de pago dan acceso al resto de zonas, y cada zona agrega obstáculos pensados para el deslizamiento, el dash o el stomp.

**Mecánicas utilizadas:**  
Correr, saltar y doble salto, deslizamiento, dash y stomp; apuntado, disparo, recarga, cambio de arma y compras con puntos (armas, munición, puertas, trampas, mejoras y pilas).

**Enemigos / obstáculos:**  
Mutantes (científicos infectados por Neuroplex) que persiguen y atacan cuerpo a cuerpo. Las puertas de pago limitan el acceso inicial. Los obstáculos de cada zona se describen en [[#Zonas de BROTE]].

**Recompensas:**  
Puntos por dañar y eliminar mutantes, y acceso a armas, mejoras, trampas y pilas mediante la economía de la partida.

**Puntos de guardado:**  
No hay guardado del avance de una partida.

**Condición de entrada:**  
Al iniciar una partida, Tannat aparece en la Sala de Contención (Zona 1) con la pistola, vida completa y 500 puntos. La primera ronda empieza a los 3 s.

**Condición de salida:**  
La partida termina cuando Tannat cae sin la pila RESPALDO instalada. No hay una salida final del laboratorio como condición de victoria.

**Eventos narrativos:**  
Los monitores («CUARENTENA», «EXPERIMENTO NEUROPLEX / CONTENCION FALLIDA»), los letreros de cada zona y los textos breves del HUD de Tannat aportan contexto sin detener el combate. Cuyus no sale del robot.

**Mapa / diagrama:**  
Planta baja y planta alta de BROTE (más vistas en [[06 - Galería de Arte]]):

![[brote-plan-ground.png]]

![[brote-plan-upper.png]]

## Zonas de BROTE

BROTE es un homenaje a Outbreak, de *Call of Duty: Advanced Warfare*: el laboratorio de Neuroplex sellado tras el brote. Tiene seis zonas y un sótano secreto, el Incinerador. Las puertas miden 8 × 8 m y el techo está sellado a 40 m.

| Zona | Cómo se entra | Obstáculos y recorrido | Compras y elementos |
|---|---|---|---|
| **Sala de Contención** (Zona 1; letrero «BROTE») | Inicio | Banco de cápsulas de 3.4 m (cobertura y percha); entrepiso de 9 m con rampa, desde el que caen mutantes; torre de monitoreo de 12 m. | Rifle y Escopeta. |
| **Administración** y Pasillo rojo | Puerta 1 | Circuito de dos rampas de deslizamiento y balcón de 6 m; el pasillo rojo en L funciona como carril de dash. | Blaster, Subfusil, ducha de descontaminación, estación de mejora y ducto al Incinerador (planta alta). |
| **Laboratorio Central** (Zona 2; Rotonda) | Puerta 2 | Muro de 22 m; pasarela a 10 m sobre rampas helicoidales; perchas de 16 m; 6 orbes de dash. | Rifle de asalto (en la pasarela), anillo electrificado (se activa desde la pasarela) e impresora 3D (posición inicial). |
| **Morgue** | Puertas 3 y 4 | Sala de doble altura con rampa a un entrepiso de 6 m; los cajones de las cámaras frías son puntos de aparición. | Escopeta de bomba. |
| **Celdas** | Puerta 5 | Pasarelas a 6 m; celda colgante con techo a 9.5 m; tanques de especímenes como perchas de 10 m; corredor de dash de 44 m. | Ametralladora, estación de mejora e interruptor del stomp. |
| **Pruebas Exo** (Hangar) | Puertas 6 y 7 | Columnas de 3, 6, 9 y 12 m hasta una grúa de 15 m; plataformas de 9 m; arcos de dash; plataforma de lanzamiento de 6 m; galería de 6 m; 3 orbes de dash. La compuerta de la bahía es punto de aparición. | Rifle de tirador, arnés Exo, estación de mejora Experimental (planta alta) y ducto al Incinerador. |
| **Incinerador** (sótano secreto, −14 m) | Solo por los ductos | Un muro triturador barre la sala en 30 s: hace 100 de daño y expulsa a Tannat. La llave del incinerador está en una cornisa de 6 m. | Llave del incinerador (desbloquea MK4) y pads de salida hacia la Sala de Contención. |

Los precios de las armas y las mejoras están en [[04 - Objetos y Coleccionables]].

### Puertas

Cada puerta se cobra una sola vez y queda abierta hasta terminar la partida.

| Puerta | Conecta | Costo |
|---|---|---:|
| 1 | Sala de Contención → Administración | 750 |
| 2 | Sala de Contención → Laboratorio Central | 1,250 |
| 3 | Administración → Morgue | 1,000 |
| 4 | Laboratorio Central → Morgue | 1,000 |
| 5 | Laboratorio Central → Celdas | 1,000 |
| 6 | Morgue (planta alta) → Pruebas Exo | 1,250 |
| 7 | Celdas → Pruebas Exo | 1,250 |

### Trampas, ductos e Incinerador

| Elemento | Dónde | Costo | Regla |
|---|---|---:|---|
| Ducha de descontaminación | Administración | 1,000 | Activa 20 s; enfriamiento de 40 s. Sus bajas no dan puntos. |
| Anillo electrificado | Laboratorio Central (se activa desde la pasarela) | 1,000 | Activo 20 s; enfriamiento de 40 s. Sus bajas no dan puntos. |
| Ducto | Planta alta de Administración y Pruebas Exo | 500 | Baja al Incinerador, que pasa a ser el punto de reaparición. |

### Aparición de mutantes

- BROTE tiene 27 puntos de aparición: 6 en la Sala de Contención, 5 en Pruebas Exo y 4 en cada una de las demás zonas. Algunos están en las plantas altas.
- Se omiten los puntos que están a menos de 12 m de Tannat.
- Solo aparecen mutantes en la zona de Tannat y en las zonas abiertas conectadas con ella.

## Flujo del nivel

```text
Inicio en la Sala de Contención → Combatir y reunir puntos → Abrir puertas hacia nuevas zonas → Comprar armas, mejoras y pilas → Continuar las rondas en las zonas abiertas → Derrota y posibilidad de reintentar
```

## PRUEBAS — Cuarto de pruebas

**Propósito:** probar todas las mecánicas en un solo sitio («todas las mecanicas en un solo sitio», según el menú).

**Estructura:** un punto central (hub), un campo de tiro, una arena, una exhibición de enemigos, una armería gratuita y un circuito de movimiento.

**Rondas:** solo empiezan desde las consolas del nivel.

## Criterios de calidad

- El objetivo es comprensible.
- Las reglas se pueden aprender.
- El desafío corresponde al nivel de progresión.
- Existe retroalimentación suficiente.
- El jugador entiende por qué tuvo éxito o fracaso.


> **Navegación:** [[00 - Índice]] · ← [[01 - Estructura del Contenido]] · [[03 - Enemigos y NPC]] →
