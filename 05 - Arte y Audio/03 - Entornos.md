# Entornos

## Descripción de la sección

Define la estética y necesidades visuales de escenarios, fondos, objetos y elementos ambientales.

## Zonas

El nivel jugable en Unity es **BROTE**: el laboratorio de Neuroplex sellado tras el brote. La ambientación post-apocalíptica ("laboratorio con brechas": techos y muros rotos hacia el cielo, óxido, agua y vegetación) se aplica zona por zona.

| Zona | Color de acento | Compras en pared | Estado del arte |
|---|---|---|---|
| Sala de Contención (inicio, Zona 1) | Rojo de emergencia y azul | Rifle y escopeta | Ambientación post-apocalíptica aplicada |
| Laboratorio Central (Zona 2) | Rojo | Rifle de asalto y la impresora 3D | Ambientación en curso |
| Morgue | Cian | Escopeta de bomba | Blockout |
| Celdas | Verde frío | Ametralladora | Blockout |
| Administración y Pasillo rojo | Blanco frío; rojo en el pasillo | — | Sellada |
| Pruebas Exo | Blanco azulado | — | Sellada |
| Incinerador (sótano) | Naranja | — | Cáscara inaccesible |

> [!warning] Recortado para la entrega (2026-11-12)
> Administración y Pruebas Exo se sellaron porque aún no estaban ambientadas; el Incinerador quedó inaccesible. Las compras de Blaster, Subfusil y Rifle de tirador salen solo de la impresora 3D. Ver [[05 - Gestión de Cambios]].

Planos, blockout y capturas: [[06 - Galería de Arte]].

![[brote-plan-ground.png]]

Puertas, obstáculos y trampas de cada zona: [[02 - Niveles]].

## Modularidad

¿Qué elementos pueden reutilizarse?

Todavía no se ha definido qué piezas del laboratorio serán modulares. La decisión depende del plano y de los modelos disponibles.

## Iluminación

Describe iluminación global, fuentes de luz y cambios durante el juego.

Iluminación fría de laboratorio con fluorescentes, zonas en penumbra y luces de emergencia rojas. Cada zona tiene su color de acento (tabla de arriba). La iluminación no cambia durante la partida. *(propuesta)*

## Efectos visuales

- [x] Partículas: fogonazo del disparo.
- [ ] Clima: no aplica (interior).
- [x] Humo y fuego de ambiente: llamas, humo, ascuas, ceniza, goteos, vapor, chispas y polvo.
- [ ] Agua
- [ ] Magia / energía
- [x] Impactos: sobre mutantes y superficies.
- [x] Atmósfera: emisores, parpadeos, balizas de alarma y lámparas que fallan.

## Recursos requeridos

Ya existen en Unity: Tannat (completo y brazos en primera persona), Cuyus, el científico infectado, las nueve armas obtenibles, el blockout de BROTE y la interfaz. Falta la ambientación post-apocalíptica de las zonas que siguen en blockout.

> [!warning] Recortado para la entrega (2026-11-12)
> Las estaciones de mejora (Pack-a-Punch) y el Cohete salieron de la partida; el código y las pruebas quedan. Ver [[05 - Gestión de Cambios]].

- **Modelos:** piezas del laboratorio (paredes, suelo, techo), cápsulas rotas, monitores, puerta de seguridad, soportes de armas, Tannat (brazos en primera persona), científicos infectados y las nueve armas obtenibles.
- **Texturas y materiales:** metal, vidrio, plástico y suciedad del brote.
- **Efectos:** fogonazo, impactos y luces de emergencia.
- **Interfaz:** iconos de vida, munición y puntos; textos de costo y de la tecla E.


> **Navegación:** [[00 - Índice]] · ← [[02 - Personajes y Animación]] · [[04 - Interfaz Visual]] →
