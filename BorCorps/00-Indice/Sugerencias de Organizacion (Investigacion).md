---
tipo: notas-gm
---

# Sugerencias de organización para el vault (investigación)

Resumen de lo que encontré buscando cómo otros GMs organizan campañas de rol en Obsidian, y cómo aplica a este vault. Ver [[Bitacora de Cambios|Bitácora de Cambios]] si algo de esto se termina implementando.

## Ronda 2 (2026-07-27): separación GM / Jugadores y "conocimiento acumulado"

El vault original separaba GM de jugadores solo con un campo `spoiler:` en el frontmatter, mezclando todo en las mismas carpetas por tema. Investigando patrones más específicos para esto, el más relevante fue [dclasair/ttrpg-campaign-vault](https://github.com/dclasair/ttrpg-campaign-vault): divide el vault en dos ramas de nivel superior, **"DM Info"** (secretos, planificación) y **"Player Info"** (mundo descubierto, personajes, sesiones), con un flujo de trabajo explícito: *"después de cada sesión, mové la información que los jugadores descubrieron de la carpeta de sesión a la subcarpeta correspondiente de Player Info"*.

Eso es exactamente lo que se implementó acá: la raíz del vault ahora tiene `GM/` y `Jugadores/` como ramas separadas, más una convención de nombres (sufijo `(Conocido)`) para que cada NPC/lugar relevante tenga una nota GM completa y una nota de jugadores que se va llenando *solo* con lo que se reveló en mesa — ver [[Indice GM]] para el detalle del mecanismo. No existe un plugin de Obsidian que automatice el "reveal progresivo"; es un patrón de convención de notas, no de tooling.

## Lo que ya estábamos haciendo bien (sigue vigente)

- **Estructura por carpetas numeradas + notas MOC** ([[Indice GM|Índice GM]] e [[Indice Jugadores|Índice Jugadores]] como hubs): patrón más recomendado para campañas de rol en Obsidian, escala bien a medida que se acumulan sesiones.
- **Plantillas reutilizables** (sesión, NPC, planeta-misión, piloto, artefacto, y ahora también las versiones "Conocido"): patrón estándar recomendado para no reinventar la estructura cada vez.

## Plugins recomendados para instalar

Ninguno es necesario para que el vault funcione — son todos community plugins de Obsidian, opcionales:

- **Dataview**: permite armar tablas y listas automáticas a partir del frontmatter YAML (por ejemplo, listar todos los NPCs con `vivo: no`, todos los fragmentos con `estado_fragmento: roto`, o todas las notas `(Conocido)` cuyo `actualizado_hasta_sesion` quedó atrás de la última sesión jugada). El frontmatter de este vault ya está pensado para esto.
- **Templater**: automatiza la creación de notas nuevas a partir de las plantillas, incluidas las de `Jugadores/` (`_Plantilla de NPC Conocido`, `_Plantilla de Lugar Conocido`, `_Plantilla de Bitacora de Sesion`).
- **Excalidraw** (opcional): útil si en algún momento querés mapear el sistema estelar o el interior de una nave/ruina a mano.
- **Kanban** (opcional): útil para llevar un tablero de "ganchos de misión pendientes / en curso / resueltos" separado del [[Registro de Fragmentos (Tracker)|tracker de fragmentos]].
- **Dice Roller**: agrega tiradas de dados dentro de las notas — se escribe algo como `dice: 1d20+2` y queda como un botón cliqueable que tira y muestra el resultado en el momento. Sirve para tiradas rápidas de NPC/ambientación directo desde una nota de `GM/06-Planetas y Misiones` o `GM/05-Sesiones` sin salir de Obsidian (las tiradas de los PJs siguen siendo en COMP/CON o físicas, esto es solo para el lado GM). Combina bien con **Fantasy Statblocks** si más adelante querés fichas de NPC con daño/ataques cliqueables en vez de placeholders de texto.

## Otras convenciones que vale la pena adoptar

- **Un vault, una campaña**: si en el futuro arrancás otra campaña de Lancer (o de otro sistema), lo más recomendado es un vault nuevo en vez de mezclar todo en este.
- **Compartir la carpeta `Jugadores/` sola, a futuro**: si más adelante el grupo quiere acceso directo (no solo pantalla compartida), la separación en carpeta propia ya deja `Jugadores/` lista para sincronizarse aparte (Syncthing, Obsidian Sync, o simplemente copiar la carpeta a un Drive compartido) sin tocar nada de `GM/`. No hace falta armarlo ahora.
- **Las notas de sesión GM (`GM/05-Sesiones`) siguen siendo la columna vertebral de la preparación** — lo nuevo es que cada una termina con un checklist "Después de jugar: actualizar Jugadores" que empuja lo revelado hacia las notas `(Conocido)`, así el hábito no depende de acordarse solo.

## Fuentes consultadas

Ronda 1:
- [Campaign Management in Obsidian — Gnome Stew](https://gnomestew.com/campaign-management-in-obsidian/)
- [Organizing Campaigns for D&D in Obsidian — phd20.com](https://phd20.com/blog/organizing-obsidian-dnd-campaigns/)
- [Using Obsidian for D&D and TTRPG Notes — GM Assistant](https://gmassistant.app/blog/using-obsidian-for-ttrpg-notes-part-1)
- [for TTRPG — Obsidian Hub](https://publish.obsidian.md/hub/04+-+Guides,+Workflows,+&+Courses/for+TTRPG)
- [obsidian-rpg-manager (plugin) — GitHub](https://github.com/carlonicora/obsidian-rpg-manager)
- [Using Obsidian for Lazy RPG Prep — Sly Flourish](https://slyflourish.com/obsidian.html)
- [COMP/CON — Massif Press](https://massif-press.itch.io/compcon)

Ronda 2:
- [ttrpg-campaign-vault (DM Info / Player Info) — dclasair, GitHub](https://github.com/dclasair/ttrpg-campaign-vault)
- [Vault Structure — Obsidian TTRPG Tutorials](https://obsidianttrpgtutorials.com/Obsidian+TTRPG+Tutorials/Getting+Started/Vault+Structure)
- [Fantasy Statblocks (plugin) — Obsidian TTRPG Community](https://github.com/Obsidian-TTRPG-Community/fantasy-statblocks)
- [Dice Roller (plugin) — Obsidian community plugin directory](https://obsidian.md/plugins?id=obsidian-dice-roller)
