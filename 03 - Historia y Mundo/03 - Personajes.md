# Personajes

## Descripción de la sección

Cada personaje importante debe tener una función clara dentro de la historia y/o la jugabilidad.

> [!info] Referencias visuales
> Todos los dibujos de esta sección son **diseños del equipo**. Están guardados en `assets/characters/`.

## Personajes

### Protagonista — Tannat

**Rol:** Protagonista y personaje controlado por el jugador.

**Función jugable:** Se controla en primera persona; el jugador ve sus brazos y, al hacer slide, sus piernas. Usa diez armas y un exotraje con doble salto, dash, slide y stomp. Acepta hasta cuatro pilas que mejoran su vida, sus armas y su movimiento.

**Función narrativa:** Funciona como armadura y mantiene con vida a Cuyus, que permanece en su interior durante toda la partida.

**Descripción física:** Robot grande y robusto. Su cabeza es una pantalla rectangular negra atravesada por una línea diagonal. El torso es ancho y tiene un compartimento frontal oscuro. Tiene rodilleras grandes y redondeadas, botas negras y manos mecánicas articuladas. En los dibujos aparece con brotes y hojas creciendo sobre su cuerpo y con un panel con luz roja en el costado, lo que sugiere que estuvo abandonado durante un tiempo.

**Personalidad:** Silencioso y protector; no se expresa con palabras.

**Motivaciones:** Proteger a Cuyus.

**Objetivos:** Sobrevivir a las hordas de mutantes y mantener a Cuyus con vida.

**Conflicto:** Las hordas de mutantes infectados por Neuroplex lo persiguen sin descanso.

**Relaciones:** Cuyus vive en su interior; depende de él para sobrevivir.

**Arco del personaje:** No aplica: al ser modo endless, no hay un arco narrativo cerrado.

**Habilidades:** Uso de diez armas; doble salto, dash, slide y stomp (el dash y el stomp dañan); regeneración de vida; espacio para cuatro pilas.

**Debilidades:** Si su vida llega a cero sin una pila RESPALDO, la partida termina y Cuyus queda desprotegida.

**Frases o tono de diálogo:** No habla ni muestra mensajes.

**Referencias visuales:**

![[tannat-cuyus-sitting.png]]
![[tannat-cuyus-looking-down.png]]

### Personaje secundario — Cuyus

**Rol:** Personaje narrativo; la niña a la que Tannat protege. No se controla por separado.

**Función jugable:** No se controla. Su cara aparece en el HUD ("NINA A BORDO") y reacciona a la partida: se pone melancólica con poca vida, llora cuando Tannat cae y celebra cada 5 bajas en combo.

**Función narrativa:** Es la razón por la que Tannat combate.

**Descripción física:** Niña de 10 años con cabello a la altura de los hombros y un fleco que le cubre parte de un ojo. Viste un vestido sin mangas de falda acampanada con un corazón en el pecho, medias largas y zapatos redondeados.

**Personalidad:** La hoja de expresiones define seis registros: melancolía, enojo contenido, locura, neutro, sonrisa infantil y desprecio. En "locura" y "desprecio" aparece una mancha negra sobre el ojo.

**Motivaciones:** Sobrevivir al virus Neuroplex.

**Objetivos:** Mantenerse con vida dentro de Tannat.

**Conflicto:** Fuera de Tannat no sobreviviría al virus.

**Relaciones:** Encontró a Tannat en el laboratorio y se refugió en su interior.

**Arco del personaje:** No aplica: al ser modo endless, no hay un arco narrativo cerrado.

**Habilidades:** Ninguna jugable.

**Debilidades:** Depende por completo de Tannat.

**Frases o tono de diálogo:** No aplica; el juego no tiene diálogos.

**Referencias visuales:**

![[cuyus-expression-sheet.png]]
![[tannat-cuyus-encounter.png]]

### Antagonista — Mutantes

**Rol:** Enemigos.

**Función jugable:** Persiguen a Tannat, lo atacan cuerpo a cuerpo y, desde la ronda 3, algunos saltan hacia él o corren. Su cantidad, vida y velocidad aumentan con cada ronda.

**Función narrativa:** Son el personal del laboratorio infectado por Neuroplex.

**Descripción física:** Científico infectado por Neuroplex, modelado en Blender en low poly: bata y ropa desgastadas, manchas de mugre y sangre (texturas de 64 px), un tumor de Neuroplex grande y un efecto de glitch (picos, remolino y destellos invertidos) que se intensifica con la "locura" de la horda. Es el único enemigo en todos los niveles.

**Personalidad:** Mente colmena: comparten la misma conducta y conocen la posición de Tannat desde que aparecen.

**Motivaciones:** Actúan impulsados por el virus Neuroplex como una mente colmena.

**Objetivos:** Alcanzar y atacar a Tannat.

**Conflicto:** No aplica.

**Relaciones:** Hostiles hacia Tannat y Cuyus.

**Arco del personaje:** No aplica.

**Habilidades:** Persecución mediante rutas de navegación, ataque cuerpo a cuerpo, salto y carrera.

**Debilidades:** La cabeza: una baja con disparo a la cabeza da más puntos.

**Frases o tono de diálogo:** No aplica.

**Referencias visuales:** Modelo `Enemy_Scientist.blend` en `ArtSource/Characters/Enemies/` del repositorio del juego.

## NPC

No se han definido NPC externos. Cuyus es el único personaje no controlado y permanece dentro de Tannat. Ver [[03 - Enemigos y NPC]].

> **Navegación:** [[00 - Índice]] · ← [[02 - Mundo]] · [[04 - Diálogos y Narrativa]] →
