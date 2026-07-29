---
tipo: notas-gm
---

# Cómo usamos COMP/CON junto con este vault

> [!tip] Regla simple
> **Obsidian es para narrativa y prep de GM. [COMP/CON](https://compcon.app) es para todo lo mecánico.** Nunca dupliques una ficha de piloto/mecha/NPC completa acá adentro — vas a terminar con dos versiones desincronizadas apenas alguien suba de nivel o cambie de loadout.

Lancer no es D&D: no hay clases de personaje, niveles, ni "armadura" como número único. Antes de crear contenido, estos son los términos que vas a ver usados en las plantillas de este vault, tal como los usa COMP/CON:

## Vocabulario Lancer (no D&D)

- **Licencia (License)**: lo que un piloto compra con LL (Licence Level) para poder usar el frame y equipo de un fabricante. No es "nivel de personaje", es acceso a catálogo.
- **Frame**: el chasis del mecha (ej. Everest, Lancaster, Barbarossa). Tiene sus propias stats (estructura, estrés, blindaje, evasión, e-defensa, capacidad de calor, sensores, velocidad, SP) y un Core System único.
- **Sistemas y Armas (Systems / Weapons)**: el loadout instalado en los *mounts* del frame (Main, Flex, Heavy, Aux, etc.).
- **Talento (Talent)**: habilidad de piloto (no de mecha), sube de rango 1-3 con LL.
- **Core Bonus**: bonus de fabricante que un piloto desbloquea con suficiente Licencia de esa marca.
- **Trasfondo (Background)**: el "origen" narrativo-mecánico del piloto, da triggers de habilidad iniciales.
- **NPC Class + Tier**: los NPCs no tienen nivel, tienen una clase (ej. Berserker, Sniper, Support) y un Tier 1/2/3 — Tier 1 es tan duro como un piloto solo, Tier 2 como un escuadrón chico, Tier 3 como un escuadrón entero. El GM arma esto en el **GM Toolkit** de COMP/CON.
- **NPC Template**: una capa opcional sobre una NPC Class (ej. Elite, Veteran) que la hace más dura sin cambiarle el rol.

## Qué vive dónde

| Contenido | Vive en |
|---|---|
| Trasfondo, motivación, arco personal de un piloto | Obsidian ([[Plantilla de Piloto]]) |
| Talentos, core bonus, triggers, HP/estructura actual del piloto | COMP/CON (Pilot Roster) |
| Pintura, apodo, personalidad del mecha | Obsidian ([[Plantilla de Mecha]]) |
| Frame, sistemas, armas, mods, SP del mecha | COMP/CON (Pilot Roster → mecha del piloto) |
| Quién es un NPC, su motivación, qué sabe | Obsidian ([[Plantilla de NPC]]) |
| NPC Class, Tier, stats de combate del NPC | COMP/CON (GM Toolkit → NPCs) |
| El encuentro de una sesión (qué NPCs salen, en qué mapa) | COMP/CON (GM Toolkit → Encounters), referenciado desde [[Plantilla de Sesion]] |

## Fuentes de datos oficiales (para consultar reglas o crear contenido homebrew)

- [COMP/CON (dev)](https://dev.compcon.app) — la app en sí: Compendio, Roster de Pilotos, GM Toolkit, Modo Activo.
- [massif-press/lancer-data](https://github.com/massif-press/lancer-data) — el JSON de todo el contenido del core book (frames, sistemas, armas, talentos, backgrounds, core bonuses) tal como lo lee COMP/CON. Útil como referencia de esquema si en algún momento armamos contenido mecánico homebrew (frame o NPC class propio de BorjusCorp) como LCP.
- [massif-press/compcon](https://github.com/massif-press/compcon) — el código fuente de la app (open source).

## Sobre contenido mecánico homebrew (a futuro)

Por ahora el objetivo del módulo homebrew es **solo narrativo/setting** — la gente que lo use arma sus pilotos con las reglas estándar de Lancer en COMP/CON. Si más adelante querés sumar algo mecánico propio de BorjusCorp (un frame corporativo, una NPC Class para VESTA, etc.), eso se empaqueta como un **LCP** (Lancer Content Pack, un .zip con JSON siguiendo el esquema de `lancer-data`) para que se importe directo en COMP/CON — es una fase aparte, no hace falta resolverla ahora.
