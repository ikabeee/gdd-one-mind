# Sistemas del Juego

## Descripción de la sección

Los sistemas son conjuntos de reglas y componentes que trabajan juntos: combate, inventario, IA, diálogo, progresión, economía, misiones, etc.

## Inventario de sistemas

| Sistema | Propósito | Dependencias | Estado |
|---|---|---|---|
| Sistema de armas e inventario | Gestionar pistola, SMG y escopeta, su compra y el límite de dos armas equipadas. | Economía (puntos) | Por desarrollar |
| Sistema de IA de mutantes | Controlar el spawn y comportamiento de mente colmena de los mutantes. | Sistema de rondas y sistema de zonas | Por desarrollar |
| Sistema de rondas | Controlar el incremento de dificultad y la cantidad de mutantes por ronda. | Sistema de IA de mutantes | Por desarrollar |
| Sistema de economía | Gestionar la obtención y gasto de puntos. | Sistema de rondas, sistema de armas | Por desarrollar |
| Sistema de zonas | Abrir la puerta entre las dos zonas y habilitar los puntos de aparición de la Zona 2. | Economía (puntos) | Por desarrollar |

## Sistemas

### Sistema de IA de mutantes

**Objetivo:**  
Hacer que los mutantes localicen y persigan al jugador de forma constante, reforzando la tensión psicológica del juego.

**Entradas:**  
Posición del jugador, punto de spawn del mutante.

**Procesamiento / reglas:**  
Al aparecer, cada mutante obtiene la posición de Tannat y calcula una ruta de navegación hacia él. Recalcula la ruta periódicamente mientras persigue. Al entrar en rango de ataque, se detiene y ataca cuerpo a cuerpo; si Tannat se aleja, vuelve a perseguir. Al recibir daño suficiente, queda eliminado y emite su evento de muerte.

**Salidas:**  
Movimiento del mutante hacia el jugador; ataque al alcanzarlo.

**Estados posibles:**  
Spawnean, persiguiendo, atacando, eliminado.

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
Los mutantes deben recorrer las dos zonas sin atravesar obstáculos, atacar dentro del rango previsto y registrar su muerte una sola vez.

### Sistema de armas e inventario

El jugador inicia con la pistola en la primera ranura. Al comprar un arma se ocupa la ranura libre; si las dos están llenas, se sustituye la activa. El sistema controla disparo, recarga, cambio de arma y munición, y actualiza el HUD. Debe impedir disparar sin munición y mantener independientes las reservas de cada arma. La pistola, la SMG y la escopeta deben distinguirse por cadencia, dispersión y alcance.

### Sistema de rondas

Al iniciar cada ronda calcula cuántos mutantes deben aparecer y su vida según el número de ronda. Lleva el conteo de enemigos pendientes de aparecer y vivos, respetando el límite de enemigos activos. Cuando ambos llegan a cero, inicia la transición entre rondas (ver [[07 - Reglas y Estados del Juego]]) y después comienza la siguiente ronda.

### Sistema de economía

Suma puntos por cada baja (100 como valor de prueba). Antes de cada compra comprueba si hay puntos suficientes: si los hay, los descuenta y confirma la compra; si no, la rechaza con aviso visual y sonoro. Los puntos se reinician a cero al comenzar una nueva partida.

### Sistema de zonas

Al comenzar, solo está habilitada la Zona 1. Pulsar E frente a la puerta comprueba los puntos, descuenta el costo una sola vez y abre el paso a la Zona 2 hasta terminar la partida. También habilita sus puntos de aparición y compras. Antes de abrirla, ni el jugador puede cruzar ni los enemigos pueden aparecer dentro de la Zona 2.

## Relaciones entre sistemas

El sistema de aparición utiliza únicamente las zonas abiertas. La IA conduce a los enemigos hasta Tannat y comunica sus bajas a rondas y economía. Los puntos permiten comprar armas, munición, mejoras y abrir la puerta; al abrirla se habilitan los puntos de aparición de la Zona 2.


> **Navegación:** [[00 - Índice]] · ← [[02 - Mecánicas]] · [[04 - Controles]] →
