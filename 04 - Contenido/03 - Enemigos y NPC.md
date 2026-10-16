# Enemigos y NPC

## Descripción de la sección

Documenta las entidades controladas por el juego y su comportamiento.

## Ficha del enemigo

### Mutante infectado por Neuroplex

**Rol de combate:**  
Enemigo cuerpo a cuerpo que presiona al jugador para que mantenga distancia.

**Comportamiento:**  
Conoce la posición de Tannat desde que aparece, lo persigue y lo ataca al alcanzarlo. La conducta es compartida por los diseños visuales de mutantes.

**Vida:**  
Aumenta con las rondas. Valor inicial y aumento pendientes de balance.

**Daño:**  
Pendiente de definir y probar.

**Defensas:**  
No se han definido defensas especiales.

**Velocidad:**  
Pendiente de definir y probar junto con la velocidad de Tannat.

**Rango de detección:**  
Los mutantes conocen la posición del jugador desde su aparición; no se plantea una fase de búsqueda.

**Ataques:**  
Cuerpo a cuerpo. Alcance, intervalo y animación pendientes.

**Debilidades:**  
No se han definido puntos débiles ni vulnerabilidades especiales.

**Recompensa:**  
Puntos por baja. El GDD propone 100 como valor inicial de prueba, no como balance definitivo.

**Estados de IA:**

```text
Aparecer → Perseguir a Tannat → Atacar al entrar en rango
                  ↑                        ↓
                  └──── Volver a perseguir si se aleja

Al agotar su vida → Eliminado
```

## Personaje no controlado por separado

**Nombre:** Cuyus.

**Función:** Es la niña a la que Tannat protege y mantiene viva.

**Ubicación:** Dentro de Tannat durante todo el juego.

**Interacción:** Su presencia forma parte de la historia.

**Diálogos:** No aplica; el juego no tiene diálogos.

**Condiciones:** Permanece dentro del robot; no se plantea acompañamiento externo.

**Recompensas / información:** No se han definido recompensas entregadas por Cuyus.


> **Navegación:** [[00 - Índice]] · ← [[02 - Niveles]] · [[04 - Objetos y Coleccionables]] →
