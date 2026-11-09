# Dirección de Arte

## Descripción de la sección

Define la identidad visual del videojuego y las reglas que deben seguir los recursos gráficos.

## Identidad visual

**Estilo:**  
Low poly en un entorno 3D, con texturas de baja resolución sin filtrado (point filter), enemigos con estética PS1 (shader `OneMind/PS1Enemy`) y una interfaz de píxel. La meta del equipo: "la estética low poly pero con la misma calidad de animaciones que un juego actual".

**Referencias:**  
Dibujos de personajes del equipo; Call of Duty: Modern Warfare (2019) para las animaciones en primera persona; Black Ops 2 Zombies y Halo 3 para el ritmo y la forma de los efectos de disparo; CICADAMATA para el aspecto plano de esos efectos.

**Sensación buscada:**  
Tensión durante la supervivencia y sensación de protección de Cuyus a través de Tannat, de acuerdo con la historia y los pilares del juego.

**Nivel de realismo:**  
Representación estilizada mediante modelos low poly.

**Formas predominantes:**  
Geometría simplificada propia del estilo low poly. Tannat es robusto y cuadrado; los científicos tienen siluetas humanas deformadas por el tumor de Neuroplex.

**Iluminación:** Luz ambiental baja, niebla casi negra y una luz de acento por zona (verde frío en las Celdas, cian en la Morgue, naranja en el incinerador, rojo en el pasillo rojo de Administración, baliza en el Laboratorio Central). Postproceso con bloom suave, viñeta, grano y dithering.

**Materiales:** Materiales URP Lit con texturas generadas en Blender (concreto, paneles de pared, metal y pintura amarilla), proyectadas en mosaicos de 4 m (2 m el metal). Los científicos usan texturas de 64 px de mugre y sangre.

## Paleta de color

*(propuesta)*

**Colores principales:** Blancos y grises fríos del laboratorio; negro para la pantalla de Tannat, como en los dibujos del equipo.

**Colores secundarios:** Verde de la vegetación que crece sobre Tannat; tonos verdosos y enfermizos para los mutantes infectados.

**Colores para información jugable:** Rojo para alertas, daño y compras rechazadas (el costo parpadea en rojo); un color claro y de alto contraste para costos y avisos de interacción.

## Reglas visuales

1. Mantener el estilo low poly en los recursos 3D del proyecto.
2. Mantener la identidad de Cuyus y Tannat y su relación: ella permanece dentro del robot.
3. Seguir la referencia de interfaz aportada por el equipo al desarrollar el HUD.

## Referencias

Diseños definitivos usados en el juego: Tannat (modelo y brazos en primera persona), Cuyus (cara en el HUD) y el científico infectado.

- Dibujos de Tannat y Cuyus del equipo: ver [[03 - Personajes]] (`assets/characters/`).
- Científico infectado: `ArtSource/Characters/Enemies/Enemy_Scientist.blend` del repositorio del juego.
- Escenario: estudio de ambientación en Blender (`ArtSource/Scenes/Outbreak/Ambience/`) y storyboard del tráiler.


> **Navegación:** [[00 - Índice]] · ← [[05 - Misiones y Desafíos]] · [[02 - Personajes y Animación]] →
