# Arquitectura Técnica

## Descripción de la sección

Explica cómo está construido técnicamente el videojuego y cómo se comunican sus componentes.

## Arquitectura

Diseño previsto: las entradas del jugador controlan movimiento, cámara y armas. Los sistemas de combate, rondas, economía y zonas actualizan el estado de la partida y la información del HUD. La organización concreta en scripts y componentes todavía debe contrastarse con el proyecto de Unity.

```text
Entrada (teclado y mouse)
  ↓
Movimiento, cámara y armas
  ↓
Sistemas: combate, rondas, economía, zonas
  ↓
Estado de la partida
  ↓
HUD
```

## Componentes principales

| Componente | Responsabilidad | Dependencias |
|---|---|---|
| Armas e inventario | Controlar las tres armas, dos ranuras, disparo, recarga y munición. | Compras, combate y HUD. |
| Zonas | Abrir la puerta y habilitar los puntos de aparición de la Zona 2. | Economía y aparición de enemigos. |
| IA y aparición de mutantes | Generar enemigos en zonas activas, perseguir y atacar a Tannat. | Rondas, zonas y combate. |
| Rondas | Controlar enemigos pendientes y vivos y el paso a la siguiente ronda. | Aparición de mutantes y registro de bajas. |
| Economía | Registrar puntos y comprobar y descontar el costo de compras. | Bajas, armas, mejoras, puerta y HUD. |

## Comunicación

Al morir un mutante, se actualizan los puntos y el conteo de enemigos de la ronda. Una compra comprueba los puntos y entrega el arma, mejora o acceso correspondiente. El HUD refleja los cambios de vida, munición y puntos. El mecanismo de comunicación entre scripts aún no está confirmado.

## Principios técnicos

- Bajo acoplamiento cuando sea razonable.
- Responsabilidades claras.
- Código mantenible.
- Datos separados de lógica cuando corresponda.
- Evitar dependencias innecesarias.


> **Navegación:** [[00 - Índice]] · ← [[04 - Guardado y Configuración]] · [[02 - Motor y Herramientas]] →
