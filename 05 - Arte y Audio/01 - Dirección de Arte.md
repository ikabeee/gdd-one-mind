# Dirección de Arte

## Descripción de la sección

Define la identidad visual del videojuego y las reglas que deben seguir los recursos gráficos.

## Identidad visual

**Estilo:**  
Low poly en un entorno 3D, con **look retro y movimiento moderno**: formas facetadas y texturas pixel art de baja resolución sin suavizado (filtrado *nearest*, al estilo PS1), sobre personajes construidos para animarse con naturalidad.

**Referencias:**  
Dibujos de personajes compartidos por el equipo y los juegos *Signalis*, *Crow Country* y *Mouthwashing* como referencia de la mezcla retro y moderna. Los nombres oficiales son Cuyus y Tannat; los nombres de los archivos de referencia no cambian esa identidad. Todo el arte actual está en [[06 - Galería de Arte]].

**Sensación buscada:**  
Tensión durante la supervivencia y sensación de protección de Cuyus a través de Tannat, de acuerdo con la historia y los pilares del juego.

**Nivel de realismo:**  
Representación estilizada mediante modelos low poly.

**Formas predominantes:**  
Geometría facetada. En los personajes, las aristas duras se biselan una vez y las extremidades tienen al menos 8 lados y se adelgazan hacia los extremos. Se evita el "look Roblox" (bloques rígidos que flotan en las articulaciones, manos de manopla y color plano uniforme) y también el extremo contrario (formas suavizadas o realistas).

**Iluminación:** Luz fría de laboratorio con zonas en penumbra. Cada zona de BROTE tiene su propio color de acento (ver [[06 - Galería de Arte]]) y el rojo de emergencia marca las alarmas.

**Materiales:**
- **Personajes:** texturas pixel art en un solo atlas (256 px para Cuyus y 512 px para Tannat), con la misma densidad de píxeles para que se vean coherentes juntos.
- **Escenario:** el laboratorio post-apocalíptico ("laboratorio con brechas") usa materiales sucios y realistas, con relieve, calcomanías y suciedad: metal, vidrio, óxido, agua y vegetación.
- **Efectos de armas:** planos y gráficos, sin realismo.

## Paleta de color

**Colores principales:** Paleta casi monocroma de blancos, grises y negros. Tannat es blanco con pantalla negra; Cuyus, gris claro con cabello negro; las armas, bloques blancos y negros.

**Colores secundarios:** Un color de acento por zona del nivel (rojo, cian, verde frío, naranja, blanco azulado) y un color propio para cada pila de Tannat (ver [[04 - Objetos y Coleccionables]]). En el escenario, el azul marca pantallas y compras en pared, y también se usa amarillo de seguridad.

**Colores para información jugable:** El HUD usa papel `#F2F2F2`, negro `#0A0A0A` y acento rojo `#D0263F`. El rojo se reserva para alertas, daño y compras rechazadas (el costo parpadea en rojo).

## Reglas visuales

1. Mantener el estilo low poly en los recursos 3D del proyecto.
2. Mantener la identidad de Cuyus y Tannat y su relación: ella permanece dentro del robot.
3. Seguir la referencia de interfaz aportada por el equipo al desarrollar el HUD.
4. Usar el rojo como acento único en los personajes: solo la luz de la pantalla de Tannat lo lleva, salvo que el rojo comunique algo.
5. Escribir sin acentos el texto que aparece en el juego, porque la fuente pixel (Pixelmix) no los dibuja.
6. Dibujar los bocetos y el storyboard en tinta: negro sobre blanco, con un solo color de acento.

## Referencias

- Galería completa (bocetos, personajes, enemigos, armas, escenario e interfaz): [[06 - Galería de Arte]].
- Dibujos de Tannat y Cuyus del equipo: ver [[03 - Personajes]] (`assets/characters/`).
- Enemigo (científico infectado), armas y escenario: renders y planos en `assets/enemies/`, `assets/weapons/` y `assets/environment/`.


> **Navegación:** [[00 - Índice]] · ← [[05 - Misiones y Desafíos]] · [[02 - Personajes y Animación]] →
