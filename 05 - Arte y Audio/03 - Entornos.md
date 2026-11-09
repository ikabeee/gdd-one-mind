# Entornos

## Descripción de la sección

Define la estética y necesidades visuales de escenarios, fondos, objetos y elementos ambientales.

## Zonas

| Zona | Estilo | Elementos | Función |
|---|---|---|---|
| Sala de Contención | Laboratorio low poly, texturizado. | Cápsulas rotas, vidrio, notas en el suelo, monitores de cuarentena, cabinas, grúa, rampa a la cubierta, puertas oscuras de aparición. | Presentar el combate y las primeras compras. |
| Administración | Oficinas y seguridad; pasillo rojo. | Piso superior con balcón, rampas, pilares. | Primera expansión barata. |
| Laboratorio Central | Laboratorio low poly, texturizado. | Tanque del experimento con la masa de Neuroplex, anillo de peligro, laboratorios de vidrio, tubos de especímenes, sala de CONTROL en el entrepiso, tuberías. | Centro del mapa y plataforma alta. |
| Morgue | Cámaras frías, sala de cómputo; luz cian. | Entrepiso y puente. | Conexión entre alas. |
| Celdas | Celdas de sujetos; luz verde fría. | Barrotes, tubos de especímenes, celda exterior del interruptor de pisotón. | Ala lejana con mejora. |
| Pruebas Exo | Hangar de robótica. | Compuerta interior, equipo del arnés. | Ala final con la mejora experimental. |
| Incinerador | Sala bajo el suelo; luz naranja. | Pared trituradora, cornisa de la llave. | Secreto. |

> [!info] Estado del texturizado (2026-11-09)
> La Sala de Contención y el Laboratorio Central ya tienen texturas y ambientación del estudio de Blender; Administración y la Morgue ya tienen ambientación. Las demás zonas conservan sus colores de greybox mientras avanza el texturizado.

## Modularidad

¿Qué elementos pueden reutilizarse?

El nivel se genera desde un script de Blender que construye las piezas por zona y las exporta como datos. Las texturas son cuatro juegos reutilizables (concreto, paneles de pared, metal y pintura amarilla) que se proyectan en mosaico, así que cualquier pieza nueva se texturiza sin UV manuales.

## Iluminación

Describe iluminación global, fuentes de luz y cambios durante el juego.

Luz ambiental baja, niebla exponencial casi negra y una luz de acento por zona. Postproceso global con bloom suave, ajustes de color, viñeta y grano. La iluminación no cambia durante la partida (el interruptor de energía planeado cambiaría el estado de la luz).

## Efectos visuales

- [x] Partículas: fogonazo, trazadores e impactos planos (flipbooks).
- [ ] Clima: no aplica (interior).
- [ ] Humo
- [x] Fuego (ambientación del laboratorio)
- [ ] Agua
- [x] Magia / energía: glitch de los científicos, descarga de la pila DESCARGA, power-ups.
- [x] Impactos: sobre mutantes y superficies.
- [x] Escombros del stomp, teñidos con la textura del suelo.

## Recursos requeridos

- **Modelos:** laboratorio de seis zonas e incinerador, cápsulas, monitores, puertas, soportes de armas, impresora 3D, estaciones de mejora y de carga, trampas, arnés, Tannat (cuerpo y brazos), científico, diez armas.
- **Texturas y materiales:** cuatro juegos del laboratorio (BaseColor, Normal, MetallicSmoothness) y las texturas de los personajes.
- **Efectos:** fogonazo, trazadores, impactos, glitch, dash y stomp.
- **Interfaz:** sprites de píxel del HUD (mira, íconos de dash, stomp y armas, placas 9-slice).
- **Pendiente:** atlas de piezas y calcomanías, y texturas de las zonas restantes.

> **Navegación:** [[00 - Índice]] · ← [[02 - Personajes y Animación]] · [[04 - Interfaz Visual]] →
