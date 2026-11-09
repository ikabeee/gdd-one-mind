# Enemigos y NPC

## Descripción de la sección

Documenta las entidades controladas por el juego y su comportamiento.

## Ficha del enemigo

### Mutante infectado por Neuroplex

**Rol de combate:**  
Enemigo cuerpo a cuerpo que presiona al jugador para que mantenga distancia. Es el único enemigo del juego: un científico de Neuroplex infectado.

**Comportamiento:**  
Emerge del suelo en 0.8 s, conoce la posición de Tannat desde que aparece, lo persigue y lo ataca al alcanzarlo. Desde la ronda 3 algunos saltan hacia Tannat y enloquecen (ver **Ataques**). Un mutante que pasa 30 s sin contacto con Tannat (10 s si está a más de 40 m) se recicla y vuelve a aparecer. Sus voces no son verbales.

**Vida:**  
150 en la ronda 1 y +100 por ronda hasta la ronda 9 (950). Desde la ronda 10, ×1.1 por ronda.

**Daño:**

| Ataque | Daño | Efecto en Tannat (100 de vida) |
|---|---:|---|
| Golpe cuerpo a cuerpo | 40 | Tres golpes lo derriban. |
| Salto | 30 | — |

**Defensas:**  
No se han definido defensas especiales.

**Velocidad:**

| Movimiento | Valor |
|---|---|
| Caminar | 4 m/s en la ronda 1, +0.3 m/s por ronda, hasta 9 m/s. |
| Correr | A más de 10 m de Tannat corre a ×1.75 de su velocidad al caminar, hasta 11.5 m/s. |
| Corredores | Desde la ronda 3 hay corredores permanentes; desde la ronda 10 corren todos. |

Tannat corre siempre a 13 m/s (ver [[02 - Mecánicas]]).

**Rango de detección:**  
Los mutantes conocen la posición del jugador desde su aparición; no se plantea una fase de búsqueda.

**Ataques:**
- **Cuerpo a cuerpo:** alcance de 1.7 m y diferencia de altura máxima de 1.8 m; se prepara en 0.4 s y espera 1 s entre ataques.
- **Salto (desde la ronda 3):** al principio salta un mutante; se suma uno cada 4 rondas, hasta 4. Salta de 3 a 9 m de distancia y hasta 6 m de altura, con un enfriamiento de 4 s ±25 %.
- **Locura (desde la ronda 3):** la proporción de mutantes enloquecidos crece hasta el 85 % en la ronda 15. Un mutante enloquecido sufre un ataque de frenesí de 1.6 s cada 5 a 12 s y después corre enfurecido durante 4 s. La locura activa un glitch al estilo PS1 en su modelo.

**Debilidades:**  
No se han definido puntos débiles ni vulnerabilidades especiales.

**Recompensa:**  
10 puntos por impacto que no mata, 60 por baja al cuerpo, 100 por baja con disparo a la cabeza y 130 por baja con stomp o dash, multiplicados por el rango de estilo. Las bajas con trampas o con PURGA no dan puntos. Al morir puede soltar un power-up. Detalle en [[06 - Economía y Recursos]].

**Estados de IA:**

```text
Emerger del suelo (0.8 s) → Perseguir a Tannat (caminar o correr) → Atacar al entrar en rango
                                   ↑                                         ↓
                                   └──────── Volver a perseguir si se aleja ─┘

Desde la ronda 3 → Saltar hacia Tannat · Frenesí y carrera enfurecida (locura)
Sin contacto 30 s (10 s si está a más de 40 m) → Reciclado
Al agotar su vida → Eliminado
```

## Personaje no controlado por separado

**Nombre:** Cuyus.

**Función:** Es la niña a la que Tannat protege y mantiene viva.

**Ubicación:** Dentro de Tannat durante todo el juego.

**Interacción:** Su presencia forma parte de la historia. Su rostro en el HUD reacciona a lo que ocurre en la partida (ver [[04 - Diálogos y Narrativa]]).

**Diálogos:** No aplica; el juego no tiene diálogos.

**Condiciones:** Permanece dentro del robot; no se plantea acompañamiento externo.

**Recompensas / información:** No se han definido recompensas entregadas por Cuyus.


> **Navegación:** [[00 - Índice]] · ← [[02 - Niveles]] · [[04 - Objetos y Coleccionables]] →
