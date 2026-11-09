# Personajes y Animación

## Descripción de la sección

Documenta cómo deben verse y comportarse visualmente los personajes.

## Requisitos por personaje

| Personaje | Modelo/Sprite | Animaciones | VFX | Estado |
|---|---|---|---|---|
| Tannat | Robot 3D low poly de 1.80 m: modelo completo para el menú y brazos en primera persona para la partida. | Por cada arma: sacar, sostener, recargar, reacomodar la mano, guardar, recoger y soltar. En el menú, una animación junto a Cuyus. | Fogonazo, trazador e impactos de cada arma. | En el juego. |
| Cuyus | Niña de 1.22 m que permanece dentro de Tannat; no se controla por separado. Su cara se arma con capas de ojos, boca y efectos. | Animación del menú con Tannat. En la partida se ve en el retrato del HUD, dibujada en la pantalla de Tannat. | 12 expresiones; el retrato se distorsiona al recibir daño. | En el juego. |
| Científico infectado (enemigo) | Único enemigo de los niveles: científico con bata gastada, tumor de Neuroplex y lentes rotos. | Reposo, caminar, correr, atacar, salto (inicio, aire y caída), frenesí, golpe leve, golpe fuerte, muerte y muerte por explosión. | Impactos rojos, ragdoll al morir y glitch de estilo PS1 según la "locura" de la horda. | En el juego. |

Las imágenes de cada personaje están en [[06 - Galería de Arte]].

## Animaciones

### Movimiento

- Idle
- Caminar
- Correr
- Saltar
- Caer

Tannat se ve en primera persona, por lo que sus animaciones se centran en brazos y armas. *(propuesta)*

### Interacción

- Tannat: pulsar E en un punto de compra (sin animación visible o con un gesto breve de la mano). *(propuesta)*
- Puerta de seguridad: animación de apertura.

### Combate

- Tannat: disparar, recargar y cambiar de arma para las diez armas del juego.
- Científicos: perseguir, saltar y atacar cuerpo a cuerpo.

### Daño

- Tannat: sacudida de cámara e indicador en pantalla. *(propuesta)*
- Científicos: golpe leve o golpe fuerte al recibir un impacto.

### Muerte / derrota

- Científicos: animación de muerte o muerte por explosión, y ragdoll.
- Tannat: la cámara cae y aparece la pantalla de derrota. *(propuesta)*

## Convenciones

Acordadas en el proyecto de Unity para Tannat, Cuyus y el científico:

| Tema | Regla |
|---|---|
| Nombres | En inglés en archivos, objetos, materiales y huesos (`Tannat`, `Girl`, `Enemy_Scientist`). |
| Herramientas | Blender, en metros y con Z hacia arriba; los personajes miran hacia −Y. |
| Exportación | FBX importado en Unity como *Humanoid*, para que las animaciones se compartan entre modelos. |
| Polígonos | Cuyus: 4,000–6,000 triángulos. Tannat: 8,000–10,000. |
| Texturas | Pixel art con filtrado *nearest*, sin mipmaps ni compresión. |
| Rigging | Hasta 4 huesos por vértice; las placas de la armadura de Tannat siguen a un solo hueso. |


> **Navegación:** [[00 - Índice]] · ← [[01 - Dirección de Arte]] · [[03 - Entornos]] →
