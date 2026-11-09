# Enemigos y NPC

## Descripción de la sección

Documenta las entidades controladas por el juego y su comportamiento.

## Ficha del enemigo

### Científico infectado por Neuroplex

**Rol de combate:**  
Enemigo cuerpo a cuerpo que presiona al jugador para que se mueva. Es el único enemigo de todos los niveles.

**Comportamiento:**  
Sale del suelo, conoce la posición de Tannat desde que aparece, lo persigue y lo ataca al alcanzarlo. Desde la ronda 3 algunos saltan hacia Tannat y otros corren; desde la ronda 10 todos corren. Tiene un efecto de glitch que crece con la "locura" de la horda.

**Vida:**  
150 en la ronda 1; +100 por ronda hasta la ronda 9; después ×1.1 por ronda (con tope para que nunca sea infinita).

**Daño:**  
40 por golpe cuerpo a cuerpo (uno por segundo); 30 por salto. Tannat tiene 100 de vida.

**Defensas:**  
No tiene defensas especiales.

**Velocidad:**  
Camina a 4 m/s, +0.3 por ronda hasta 9 m/s. Al correr, ×1.75 con tope de 11.5 m/s. Tannat corre a 13 m/s.

**Rango de detección:**  
Conoce la posición del jugador desde su aparición; no hay fase de búsqueda.

**Ataques:**  
- Golpe cuerpo a cuerpo: alcance de 1.7 m, preparación de 0.4 s.
- Salto (desde la ronda 3): de 3 a 9 m de distancia y hasta 6 m de altura, preparación de 0.35 s, enfriamiento de 4 s. Hay de 1 a 4 saltadores según la ronda.

**Debilidades:**  
La cabeza (más puntos por baja), el stomp, el dash y las trampas.

**Recompensa:**  
10 puntos por impacto; 60 por baja, 100 con disparo a la cabeza y 130 en movimiento. Puede soltar un power-up.

**Estados de IA:**

```text
Salir del suelo → Perseguir a Tannat (caminando o corriendo) → Atacar al entrar en rango
                       ↑            ↓                                  ↓
                       │      Saltar si está a 3–9 m (ronda 3+)        │
                       └──── Volver a perseguir si se aleja ←──────────┘

Sin contacto 30 s (o 10 s a más de 40 m) y fuera de vista → Reaparecer cerca del jugador
Al agotar su vida → Eliminado (cadáver 3 s)
```

### Científico EMZ (planeado)

Variante visualmente distinta (arcos eléctricos en el Neuroplex) que aparecería desde la ronda 8 en una parte pequeña de la horda. Su golpe, y atravesarlo con dash, desactivarían el dash durante 5 s. Aún no está implementado.

## Personaje no controlado por separado

**Nombre:** Cuyus.

**Función:** Es la niña a la que Tannat protege y mantiene viva.

**Ubicación:** Dentro de Tannat durante todo el juego; su cara aparece en el HUD.

**Interacción:** Su cara reacciona a la partida (poca vida, caída de Tannat, combos de bajas).

**Diálogos:** No aplica; el juego no tiene diálogos.

**Condiciones:** Permanece dentro del robot; no hay acompañamiento externo.

**Recompensas / información:** No entrega recompensas.

> **Navegación:** [[00 - Índice]] · ← [[02 - Niveles]] · [[04 - Objetos y Coleccionables]] →
