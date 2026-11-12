# Sistemas del Juego

## Descripción de la sección

Los sistemas son conjuntos de reglas y componentes que trabajan juntos: combate, inventario, IA, diálogo, progresión, economía, misiones, etc.

## Inventario de sistemas

| Sistema | Propósito | Dependencias | Estado |
|---|---|---|---|
| Sistema de armas e inventario | Gestionar las nueve armas, su compra, munición y reposición, y el límite de dos armas equipadas. | Economía (puntos) | Implementado en Unity |
| Sistema de IA de mutantes | Controlar la aparición y el comportamiento de mente colmena de los mutantes. | Sistema de rondas y sistema de zonas | Implementado en Unity |
| Sistema de rondas | Controlar el incremento de dificultad y la cantidad de mutantes por ronda. | Sistema de IA de mutantes | Implementado en Unity |
| Sistema de economía | Gestionar la obtención y gasto de puntos. | Sistema de rondas, sistema de armas | Implementado en Unity |
| Sistema de zonas | Abrir las tres puertas de BROTE y limitar la aparición a la zona de Tannat y a las zonas abiertas conectadas con ella. | Economía (puntos) | Implementado en Unity |

## Sistemas

### Sistema de IA de mutantes

**Objetivo:**  
Hacer que los mutantes localicen y persigan al jugador de forma constante, reforzando la tensión psicológica del juego.

**Entradas:**  
Posición del jugador, punto de aparición del mutante.

**Procesamiento / reglas:**  
Al aparecer, cada mutante emerge del suelo en 0.8 s, se dirige hacia Tannat y lo sigue mientras se mueve; corre cuando está a más de 10 m. Al entrar en rango de ataque, se detiene y ataca cuerpo a cuerpo; si Tannat se aleja, vuelve a perseguir. Desde la ronda 3 algunos saltan hacia Tannat y enloquecen. Un mutante que pasa 30 s sin contacto (10 s si está a más de 40 m) se recicla. Al recibir daño suficiente, queda eliminado y emite su evento de muerte. Valores en [[03 - Enemigos y NPC]].

**Salidas:**  
Movimiento del mutante hacia el jugador; ataque al alcanzarlo.

**Estados posibles:**  
Apareciendo, persiguiendo, saltando, atacando, en frenesí, eliminado.

**Dependencias:**  
El sistema de rondas determina la cantidad de enemigos y el sistema de zonas limita los puntos de aparición a las áreas desbloqueadas.

**Interacciones:**  
Con el sistema de combate/disparo del jugador y con el sistema de economía (al morir, otorga puntos).

**Datos que necesita:**  
Posición de Tannat, puntos de aparición, velocidad, daño y vida del mutante según la ronda.

**Datos que genera:**  
Eventos de muerte (para otorgar puntos), eventos de daño al jugador.

**Riesgos:**  
Acumulación de mutantes en la puerta, atascos en esquinas y pérdida de rendimiento con muchos enemigos activos.

**Criterios de aceptación:**  
Los mutantes deben recorrer todas las zonas abiertas sin atravesar obstáculos, atacar dentro del rango previsto y registrar su muerte una sola vez.

### Sistema de armas e inventario

El jugador inicia con la pistola en la primera ranura. Al comprar un arma se ocupa la ranura libre; si las dos están llenas, se sustituye la activa. El sistema controla disparo, recarga, cambio de arma y munición, y actualiza el HUD. Debe impedir disparar sin munición y mantener independientes las reservas de cada arma. Las armas deben distinguirse por modo de disparo (semiautomático, automático o perdigones), cadencia, dispersión y alcance.

### Sistema de rondas

Al iniciar cada ronda calcula cuántos mutantes deben aparecer y su vida según el número de ronda. Lleva el conteo de enemigos pendientes de aparecer y vivos, respetando el límite de enemigos activos. Cuando ambos llegan a cero, inicia la transición entre rondas (ver [[07 - Reglas y Estados del Juego]]) y después comienza la siguiente ronda.

La primera ronda empieza a los 3 s y entre rondas hay 2 s de pausa. Puede haber como máximo 32 mutantes vivos a la vez. El retraso de aparición es de 2 s, ×0.95 por ronda, con un mínimo de 0.1 s.

| Ronda | 1 | 2 | 3 | 4 | 5 | 6 | 10 |
|---|---:|---:|---:|---:|---:|---:|---:|
| Mutantes | 6 | 8 | 13 | 18 | 24 | 28 | 33 |

Desde la ronda 6, la horda es 24 + redondear(3 × r / 5 × f), con f = 1 antes de la ronda 10 y f = 0.15 × r desde la ronda 10.

### Sistema de economía

Suma 10 puntos por impacto, 60 por baja, 100 por baja con disparo a la cabeza y 130 por baja con stomp o dash, multiplicados por el rango de estilo (ver [[06 - Economía y Recursos]]). Antes de cada compra comprueba si hay puntos suficientes: si los hay, los descuenta y confirma la compra; si no, la rechaza con aviso visual y sonoro. Los puntos se reinician a 500 al comenzar una nueva partida.

### Sistema de zonas

Al comenzar, solo está habilitada la Sala de Contención (Zona 1). Pulsar E frente a una puerta comprueba los puntos, descuenta el costo una sola vez y abre el paso hasta terminar la partida (puertas y costos en [[02 - Niveles]]). También habilita las compras de la zona nueva. Solo aparecen mutantes en la zona de Tannat y en las zonas abiertas conectadas con ella, y se omiten los puntos de aparición a menos de 12 m de Tannat. Antes de abrir una puerta, el jugador no puede cruzarla.

## Relaciones entre sistemas

El sistema de aparición utiliza la zona de Tannat y las zonas abiertas conectadas con ella. La IA conduce a los enemigos hasta Tannat y comunica sus bajas a rondas y economía. Los puntos permiten comprar armas, munición y pilas y abrir puertas; al abrir una puerta, la zona nueva puede generar mutantes.


> **Navegación:** [[00 - Índice]] · ← [[02 - Mecánicas]] · [[04 - Controles]] →
