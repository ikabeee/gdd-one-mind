# Personajes y Animación

## Descripción de la sección

Documenta cómo deben verse y comportarse visualmente los personajes.

## Requisitos por personaje

| Personaje | Modelo/Sprite | Animaciones | VFX | Estado |
|---|---|---|---|---|
| Tannat | Robot 3D low poly (Blender). En primera persona se ven sus brazos, tomados de su propio modelo, y la pelvis y las piernas bajo la cámara al hacer slide. | Brazos por arma: tomar, disparar, apuntar, recargar (vacío y con bala), correr y dash. | Fogonazo, trazador, impactos, efectos de dash y stomp, glitch del HUD al recibir daño. | Implementado |
| Cuyus | Cara en un atlas de expresiones de píxel, mostrada en el HUD. | 12 expresiones: neutral, sonrisa infantil, melancolía, enojo contenido, desprecio, locura, feliz, brillo, sorpresa, puchero, sonrojo y llanto cómico. | Ninguno. | Implementado |
| Científico infectado | Modelo low poly con rig humanoide de 29 huesos, 12 materiales y ragdoll. | Salir del suelo, caminar, correr, saltar, atacar y morir (clips compartidos por retarget). | Glitch PS1 (picos, remolino y destellos invertidos); impactos distintos en carne y en superficies. | Implementado |

## Animaciones

### Movimiento

- Idle
- Caminar
- Correr
- Saltar
- Caer
- Slide (se ven las piernas de Tannat)
- Dash (la mano se mantiene sobre el arma)

### Interacción

- Tannat: pulsar E en un punto de compra.
- Puertas de seguridad, impresora 3D (imprimiendo, ofreciendo, moviéndose) y pared trituradora del incinerador.

### Combate

- Tannat: disparar, apuntar con miras de hierro (el cohete no usa mira de hierro), recargar y cambiar de arma, con un lenguaje de recarga inspirado en Modern Warfare (2019). Cada arma tiene su recarga: la ametralladora cambia la caja de munición, la escopeta de bomba mete los cartuchos a mano y los brazos no atraviesan el arma.
- Científicos: perseguir, saltar y atacar cuerpo a cuerpo.

### Daño

- Tannat: glitch en el HUD, cuadro de impacto y reacción de Cuyus.
- Científicos: reacción al impacto.

### Muerte / derrota

- Científicos: ragdoll; el cadáver dura 3 s.
- Tannat: el mundo sigue y la cámara puede mirar alrededor; aparece "HAS CAIDO" con el resumen. Cuyus llora.

## Convenciones

- Los modelos se construyen con scripts de Python en Blender (`ArtSource/Characters/.../Tools/`) y se exportan como FBX a `Assets/_Game/Art/Characters/`.
- Los enemigos usan los nombres de huesos del esqueleto compartido para poder reutilizar `Enemy_Animations.fbx`.
- Los controladores de animación (Animator) de primera persona se generan desde el editor y se conservan al regenerar.

> **Navegación:** [[00 - Índice]] · ← [[01 - Dirección de Arte]] · [[03 - Entornos]] →
