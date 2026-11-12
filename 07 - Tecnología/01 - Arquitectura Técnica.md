# Arquitectura Técnica

## Descripción de la sección

Explica cómo está construido técnicamente el videojuego y cómo se comunican sus componentes.

## Arquitectura

Código organizado por funcionalidad (`Scripts/<Función>`), con inyección de dependencias en raíces de composición (`GameLifetimeScope` y un scope por escena), sin GameManager ni service locator. Las entradas del jugador controlan movimiento, cámara y armas; combate, rondas, economía y zonas actualizan el estado de la partida y el HUD. Escenas, HUD y nivel generados por builders de editor.

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
| Armas e inventario | Controlar las nueve armas obtenibles, dos ranuras, disparo, recarga y munición. | Compras, combate y HUD. |
| Zonas | Abrir las tres puertas de pago y limitar la aparición a la zona de Tannat y a las zonas abiertas conectadas con ella. | Economía y aparición de enemigos. |
| Pilas, impresora y power-ups | Vender pilas desde la ronda 1, imprimir armas en la Rotonda y soltar power-ups por baja. | Economía, HUD y combate. |
| IA y aparición de mutantes | Generar enemigos en zonas activas, perseguir y atacar a Tannat. | Rondas, zonas y combate. |
| Rondas | Controlar enemigos pendientes y vivos y el paso a la siguiente ronda. | Aparición de mutantes y registro de bajas. |
| Economía | Registrar puntos y comprobar y descontar el costo de compras. | Bajas, armas, mejoras, puerta y HUD. |

## Comunicación

Al morir un mutante, se actualizan los puntos y el conteo de enemigos de la ronda. Una compra comprueba los puntos y entrega el arma, la pila o el acceso correspondiente. El HUD refleja los cambios de vida, munición, puntos y pilas. Las dependencias se inyectan por constructor en las raíces de composición; las vistas reportan intención y los controladores deciden.

## Principios técnicos

- Bajo acoplamiento cuando sea razonable.
- Responsabilidades claras.
- Código mantenible.
- Datos separados de lógica cuando corresponda.
- Evitar dependencias innecesarias.


> **Navegación:** [[00 - Índice]] · ← [[04 - Guardado y Configuración]] · [[02 - Motor y Herramientas]] →
