# Personajes y Animación

## Descripción de la sección

Documenta cómo deben verse y comportarse visualmente los personajes.

## Requisitos por personaje

| Personaje | Modelo/Sprite | Animaciones | VFX | Estado |
|---|---|---|---|---|
| Tannat | Robot 3D low poly de 1.80 m: modelo completo para el menú y brazos (v5) y piernas en primera persona para la partida. | Por cada arma: sacar, sostener, disparar, recargar (también en vacío), reacomodar la mano, guardar, recoger y soltar, más inspección, swipe, stomp, aterrizaje y salto. En el menú, trepa junto a Cuyus; en la derrota, apagado. | Fogonazo, trazador e impactos de cada arma. | En el juego. |
| Cuyus | Niña de 1.22 m que permanece dentro de Tannat; no se controla por separado. Su cara se arma con capas de ojos, boca y efectos. | Animación del menú con Tannat; instalación de pilas en primera persona. En la partida se ve en el retrato del HUD, dibujada en la pantalla de Tannat. | 12 expresiones; el retrato se distorsiona al recibir daño. | En el juego. |
| Científico infectado (enemigo) | Único enemigo de los niveles: científico con bata gastada, tumor de Neuroplex y lentes rotos. | Reposo, caminar (y variante), correr, carrera, atacar, salto (inicio, aire y caída), frenesí, golpe leve, golpe fuerte, tres retrocesos, muerte y muerte por explosión, trepar por ventana, arrastre y ataque arrastrado, y caída al arrastre. | Impactos rojos, ragdoll al morir y glitch de estilo PS1 según la "locura" de la horda. | En el juego. |

Las imágenes de cada personaje están en [[06 - Galería de Arte]].

## Animaciones

### Movimiento

Las piernas en primera persona animan reposo, caminar, correr, saltar, aterrizar, deslizarse, dash y stomp. Los brazos animan reposo, disparo, inspección, swipe, stomp, aterrizaje y salto, más sostener, disparar, equipar, guardar, recoger, soltar, reacomodar y recargar por cada arma (también en vacío para seis de ellas).

### Interacción

- Tannat: al pulsar E en una máquina de pilas, el arma baja, Tannat lanza la pila con la mano izquierda, Cuyus sube desde el borde inferior de la pantalla, la atrapa en el aire y vuelve a esconderse; luego el arma vuelve. La pila funciona desde que se asienta, a los 2.5 s.
- Puerta de seguridad: animación de apertura.

### Combate

- Tannat: disparar, recargar y cambiar de arma para las nueve armas obtenibles del juego.
- Científicos: perseguir, saltar y atacar cuerpo a cuerpo.

> [!warning] Recortado para la entrega (2026-11-12)
> El Cohete salió de la partida y de la impresora porque el objeto no estaba completo. Ver [[05 - Gestión de Cambios]].

### Daño

- Tannat: efecto de glitch e indicador en pantalla.
- Científicos: golpe leve o golpe fuerte al recibir un impacto.

### Muerte / derrota

- Científicos: animación de muerte o muerte por explosión, y ragdoll.
- Tannat: la cámara cae en primera persona y aparece «GAME OVER» con las rondas sobrevividas.

## Convenciones

Acordadas en el proyecto de Unity para Tannat, Cuyus y el científico:

| Tema | Regla |
|---|---|
| Nombres | En inglés en archivos, objetos, materiales y huesos (`Tannat`, `Girl`, `Enemy_Scientist`). |
| Herramientas | Blender, en metros y con Z hacia arriba; los personajes miran hacia −Y. |
| Exportación | FBX importado en Unity como *Humanoid*, para que las animaciones se compartan entre modelos. |
| Polígonos | Cuyus: 4,000–6,000 triángulos. Tannat: 8,000–10,000. |
| Texturas | Pixel art con filtrado *nearest*, sin mipmaps ni compresión. |
| Rigging | Hasta 4 huesos por vértice; las placas de la armadura de Tannat siguen a un solo hueso. Tannat, Cuyus y el científico usan un solo rig para el juego y el tráiler. |


> **Navegación:** [[00 - Índice]] · ← [[01 - Dirección de Arte]] · [[03 - Entornos]] →
