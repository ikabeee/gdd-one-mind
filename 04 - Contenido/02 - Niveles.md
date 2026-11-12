# Niveles

## Descripción de la sección

Cada nivel debe documentar su propósito jugable, estructura, dificultad, contenido y condiciones de entrada/salida.

El juego tiene un nivel jugable: **BROTE**, el laboratorio de Neuroplex. La distribución de zonas, puertas y obstáculos de BROTE está en [[#Zonas de BROTE]].

## BROTE — Laboratorio de Neuroplex

**Objetivo principal:**  
Sobrevivir al mayor número de rondas mientras Tannat protege a Cuyus en su interior.

**Objetivos secundarios:**  
Reunir puntos, conseguir armamento y abrir las puertas hacia las demás zonas para disponer de más espacio.

**Duración estimada:**  
Entre 5 y 15 minutos como referencia de prueba del GDD. La partida puede extenderse mientras el jugador sobreviva.

**Dificultad:**  
Aumenta por ronda mediante la cantidad, la vida y la velocidad de los mutantes (ver [[03 - Enemigos y NPC]]); no depende de la zona.

**Mecánicas introducidas:**  
En la Sala de Contención (Zona 1) se presentan el movimiento, el disparo y las compras en pared. Las puertas de pago dan acceso al resto de zonas, y cada zona agrega obstáculos pensados para el deslizamiento, el dash o el stomp.

**Mecánicas utilizadas:**  
Correr, saltar y doble salto, deslizamiento, dash y stomp; apuntado, disparo, recarga, cambio de arma y compras con puntos (armas, munición, puertas, trampas y pilas).

**Enemigos / obstáculos:**  
Mutantes (científicos infectados por Neuroplex) que persiguen y atacan cuerpo a cuerpo. Las puertas de pago limitan el acceso inicial. Los obstáculos de cada zona se describen en [[#Zonas de BROTE]].

**Recompensas:**  
Puntos por dañar y eliminar mutantes, y acceso a armas, trampas y pilas mediante la economía de la partida.

**Puntos de guardado:**  
No hay guardado del avance de una partida.

**Condición de entrada:**  
Al iniciar una partida, Tannat aparece en la Sala de Contención (Zona 1) con la pistola, vida completa y 500 puntos. La primera ronda empieza a los 3 s.

**Condición de salida:**  
La partida termina cuando Tannat cae sin la pila RESPALDO instalada. No hay una salida final del laboratorio como condición de victoria.

**Eventos narrativos:**  
El laboratorio vestido cuenta la historia sin detener el combate: equipo, restos del experimento y monitores apagados. Cuyus no sale del robot.

**Mapa / diagrama:**  
Planta baja y planta alta de BROTE (más vistas en [[06 - Galería de Arte]]):

![[brote-plan-ground.png]]

![[brote-plan-upper.png]]

Estos planos muestran el nivel antes de la entrega: Administración, Pruebas Exo y el Incinerador con sus estaciones, los puestos extra de la impresora y los orbes de dash ya no están en la partida.

## Zonas de BROTE

BROTE es un homenaje a Outbreak, de *Call of Duty: Advanced Warfare*: el laboratorio de Neuroplex sellado tras el brote. Tiene cuatro zonas abiertas. Las puertas miden 8 × 8 m y el techo está sellado a 40 m.

> [!warning] Recortado para la entrega (2026-11-12)
> Administración y Pruebas Exo quedaron selladas para la entrega con persianas de acero, vallas de CUARENTENA y cinta de peligro; con ellas salieron la ducha de descontaminación, la estación de mejora de Administración, los puestos extra de la impresora, los orbes de dash y 9 puntos de aparición. Ver [[05 - Gestión de Cambios]].

| Zona | Cómo se entra | Obstáculos y recorrido | Compras y elementos |
|---|---|---|---|
| **Sala de Contención** (Zona 1; letrero «BROTE») | Inicio | Banco de cápsulas de 3.4 m (cobertura y percha); entrepiso de 9 m con rampa; torre de monitoreo de 12 m. | Rifle y Escopeta (pared); pilas FILTRO y RESPALDO; 6 puntos de aparición. |
| **Laboratorio Central** (Zona 2; Rotonda) | Puerta 2 (1,250) | Tanque al centro; pasarela a 10 m sobre rampas helicoidales; perchas de 16 m; 36 vidrios rompibles. | Rifle de asalto (pared, en la pasarela); pila RAFAGA; impresora 3D; anillo electrificado (se activa desde la pasarela); 4 puntos de aparición. |
| **Morgue** | Puerta 4 (1,000) | Sala de doble altura con rampa a un entrepiso de 6 m; los cajones de las cámaras frías son puntos de aparición. | Escopeta de bomba (pared); pilas DESCARGA y SERVO; 4 puntos de aparición. |
| **Celdas** | Puerta 5 (1,000) | Pasarelas a 6 m; celda colgante con techo a 9.5 m; tanques de especímenes como perchas de 10 m; corredor de dash de 44 m. | Ametralladora (pared); pilas BLINDAJE y PISTON; interruptor del stomp; 4 puntos de aparición. |
| **Incinerador** (sótano, −14 m) | Sin acceso | Cascarón de decorado bajo el nivel, sin ductos ni llave. | — |

Los precios de las armas están en [[04 - Objetos y Coleccionables]].

### Puertas

Cada puerta se cobra una sola vez y queda abierta hasta terminar la partida.

| Puerta | Conecta | Costo |
|---|---|---:|
| 2 | Sala de Contención → Laboratorio Central | 1,250 |
| 4 | Laboratorio Central → Morgue | 1,000 |
| 5 | Laboratorio Central → Celdas | 1,000 |

Las puertas 1, 3, 6 y 7 están selladas con persianas de acero y vallas de CUARENTENA; no se pueden abrir.

### Trampas

| Elemento | Dónde | Costo | Regla |
|---|---|---:|---|
| Anillo electrificado | Laboratorio Central (se activa desde la pasarela) | 1,000 | Activo 20 s; enfriamiento de 40 s. Sus bajas no dan puntos. |

### Aparición de mutantes

- BROTE tiene 18 puntos de aparición: 6 en la Sala de Contención (5 ventanas y 1 en el suelo) y 4 en cada una de las demás zonas abiertas. Algunos están en las plantas altas.
- Se omiten los puntos que están a menos de 12 m de Tannat.
- Solo aparecen mutantes en la zona de Tannat y en las zonas abiertas conectadas con ella.

## Flujo del nivel

```text
Inicio en la Sala de Contención → Combatir y reunir puntos → Abrir puertas hacia nuevas zonas → Comprar armas, munición y pilas → Continuar las rondas en las zonas abiertas → Derrota y posibilidad de reintentar
```

## PRUEBAS — Cuarto de pruebas

Era un cuarto de pruebas con todas las mecánicas en un solo sitio, con rondas que solo empezaban desde sus consolas. Ya no se puede entrar desde el menú: «Jugar» lleva directo a BROTE.

> [!warning] Recortado para la entrega (2026-11-12)
> El nivel de pruebas salió del menú para la entrega; la escena sigue en el proyecto. Ver [[05 - Gestión de Cambios]].

## Criterios de calidad

- El objetivo es comprensible.
- Las reglas se pueden aprender.
- El desafío corresponde al nivel de progresión.
- Existe retroalimentación suficiente.
- El jugador entiende por qué tuvo éxito o fracaso.


> **Navegación:** [[00 - Índice]] · ← [[01 - Estructura del Contenido]] · [[03 - Enemigos y NPC]] →
