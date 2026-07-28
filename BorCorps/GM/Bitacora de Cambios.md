---
tipo: notas-gm
---

# Bitácora de Cambios

Registro de decisiones de diseño importantes y por qué se tomaron — útil para no olvidar el razonamiento detrás de un cambio cuando se retoma el vault meses después.

## 2026-07-27 — Creación del vault

Vault inicial armado con la estructura completa: 11 carpetas, notas de mundo, BorjusCorp, mitología de Borhamus, los 5 arcos, plantillas de sesión/planeta-misión/NPC/piloto/artefacto, y el tracker de fragmentos. Ver [[Sugerencias de Organizacion (Investigacion)|Sugerencias de Organización]] para el resumen de investigación sobre buenas prácticas de Obsidian para RPGs que informó la estructura.

Supuestos de worldbuilding tomados en esta pasada (todos editables, ver [[Indice GM|Índice GM]] y cada nota de mitología/facción para el detalle):

- 7 fragmentos de alma (dentro del rango 6-8 pedido).
- El Corredor como brazo estelar aislado que justifica el poder regional de BorjusCorp.
- Ritual de invocación requiere ≥5 de 7 fragmentos + sitio precursor adecuado + el cuerpo petrificado de Borhamus.

## 2026-07-27 — Reorganización GM / Jugadores

Se restructuró el vault de organización por tema a organización por audiencia: todo pasó a vivir bajo `GM/` (nunca compartir pantalla) o `Jugadores/` (siempre seguro), con `00-Indice/` como raíz de ambos índices. Se agregó la convención de notas `(Conocido)` — una ficha de "lo que saben hasta ahora" por cada NPC/lugar relevante, distinta de su nota GM completa — para que los links en material de jugadores (Bitácoras de Sesión) lleven a información filtrada, no a la verdad completa. Detalle del razonamiento y de las fuentes en [[Sugerencias de Organizacion (Investigacion)|Sugerencias de Organización]].

Como todavía no se jugó ninguna sesión en la mesa real, las fichas `(Conocido)` de ejemplo ([[VESTA (Conocido)]], [[Kharnis (Conocido)]]) se dejaron con solo lo predeterminado y secciones "completar después de jugar" — no se inventó ningún resultado de sesión.

## 2026-07-28 — Rediseño narrativo: Prólogo + 3 arcos, facciones rivales, disparadores en vez de conteo fijo

El usuario compartió referencias de otros GMs usando Obsidian para TTRPG y pidió analizarlas antes de tocar nada — la investigación confirmó que el modelo `GM/`↔`Jugadores/` + `(Conocido)` ya construido coincide con la práctica estándar, así que no cambió la arquitectura del vault. Lo que sí cambió fue el contenido narrativo:

- Los 5 arcos viejos (`Arco I - Contratos`, `Arco II - Grietas`, `Arco III - Revelacion`, `Arco IV - Eleccion`) se consolidaron en 3: [[Arco 1 - El Inicio]], [[Arco 2 - Las Facciones]], [[Arco 3 - La Decision]] (más el Prólogo, que se mantuvo). Se agregó [[Motor de Misiones]] como la fórmula repetible detrás de cada misión: objetivo (gema/artefacto o info de una) + método + complicación + consecuencias + chequeo de disparador de arco.
- **Corrección importante del usuario tras la primera versión del plan**: el pase de un arco a otro no es por cantidad fija de misiones/sesiones ni por LL — es un disparador narrativo que el GM decide libremente cuándo dar por cumplido. La tabla de "LL por sesión" pasó a ser una escala orientativa, no un objetivo. Las misiones pueden repetirse en un mismo planeta o abrir viaje a planetas nuevos sin cantidad fija.
- Se agregaron 3 facciones rivales confirmadas por el usuario en `GM/08-Facciones Rivales`: [[Custodios del Silencio]] (quieren destruir las gemas), [[Hijos del Alba Oscura]] (culto cismático fanático que también quiere revivir a Borhamus por su cuenta) y [[El Gremio de la Cosecha]] (mercaderes amorales). Cada una queda documentada a nivel de identidad; los NPCs concretos (líderes, recurrentes, enemigos fuertes) quedan marcados explícitamente para completar más adelante, no se inventaron en esta pasada.
- Se agregó el mecanismo de giro de [[VESTA - IA Capitana de la Custodia|VESTA]]: aliada por defecto (`actitud_hacia_grupo`), con triggers documentados para pasar a `sospecha` y `hostil` en el Arco 3.
- Se agregó el estado `desestabilizándose` a [[Los Fragmentos de Alma]] (intermedio entre `contenido` y `roto`), estrenado en la nueva [[Mision 02 - Ilsara]] — planeta de nativos primitivos cuyo "Faro" se está apagando gradualmente.
- Se agregó la sección "Consecuencias de éxito / fracaso" como estándar en la plantilla de misión y se retrofiteó en [[Mision 01 - Kharnis]] y el Prólogo (incluida la consecuencia de derrota conectando con [[El Gremio de la Cosecha]]).

## 2026-07-28 — Aplanado total de carpetas + patrón Template/Database con Dataview + git

El usuario pidió una nueva pasada de investigación (inspirada en un video de YouTube sobre el patrón "Template + Database" para TTRPG en Obsidian) porque las 17 subcarpetas numeradas (10 en `GM/`, 6 en `Jugadores/`, más `00-Indice/`) resultaban abrumadoras de navegar. Ver [[Sugerencias de Organizacion (Investigacion)|Sugerencias de Organización]], Ronda 3, para las fuentes.

Cambios:

- **Se eliminaron todas las subcarpetas.** `GM/` y `Jugadores/` ahora son carpetas planas — cada nota vive directo ahí adentro, sin nivel intermedio. La carpeta `00-Indice/` desapareció: `Indice GM.md` y `Sugerencias de Organizacion.md` pasaron a `GM/`, `Indice Jugadores.md` pasó a `Jugadores/`. La separación GM/Jugadores en sí **no se tocó** — sigue siendo la única división real, porque es una cuestión de spoilers, no de organización.
- **Se reemplazaron los índices manuales por notas "Database" con Dataview**: `Database - NPCs`, `Database - Planetas y Misiones`, `Database - Facciones Rivales`, `Database - Artefactos`, `Database - Sesiones` (en `GM/`) y `Database - NPCs Conocidos`, `Database - Lugares Conocidos`, `Database - Bitacora de Sesiones`, `Database - Personajes (PJs)` (en `Jugadores/`). Cada una es una tabla `dataview` que filtra por el campo `tipo:` que ya existía en el frontmatter de cada plantilla — no hay que tocar ninguna Database a mano al crear una nota nueva, con que tenga el `tipo:` correcto ya aparece solita. Las queries excluyen archivos cuyo nombre empieza con "Plantilla" para que las plantillas no se listen a sí mismas como si fueran instancias.
- Ningún contenido narrativo cambió — esto fue puramente estructural. Los wikilinks `[[Nombre]]` de Obsidian resuelven por nombre de nota, no por carpeta, así que mover archivos no rompió ningún link existente.
- **Se inicializó git** en la raíz del proyecto (`E:\BorCorps - Lancer Campain`, ver [[Sugerencias de Organizacion (Investigacion)|Sugerencias de Organización]] para el detalle del `.gitignore`) con un commit baseline antes de aplanar, para poder deshacer si algo salía mal. El objetivo final sigue siendo publicar esto como módulo homebrew narrativo gratuito de Lancer en GitHub (repo: `BorCops---HomeBrew-Lancer-Campain`) — por ahora sin contenido mecánico (LCP/COMP-CON), eso queda para una fase futura si se decide sumarlo.

## 2026-07-28 — Alineación con el vocabulario y sistema real de Lancer (COMP/CON)

El usuario marcó algo importante: Lancer no es D&D, y las plantillas no debían quedar genéricas. Se investigó [dev.compcon.app](https://dev.compcon.app) (la herramienta oficial) y el repo [massif-press/lancer-data](https://github.com/massif-press/lancer-data) (el JSON de datos del core book: frames, sistemas, armas, talentos, backgrounds, core bonuses) para confirmar el vocabulario correcto: Licencia, Frame, NPC Class + Tier, Talento, Core Bonus, Trasfondo — nada de "clase y nivel" ni "armadura" como en D&D.

Cambios:

- [[Plantilla de NPC]] sumó `npc_clase_comp_con`, `tier` y `enlace_comp_con` al frontmatter, más una sección aclarando que la ficha de combate real se arma en el GM Toolkit de COMP/CON, no en Obsidian.
- [[Plantilla de Piloto]] sumó `frame_principal`, `licencia_activa`, `enlace_comp_con`.
- Se creó [[Plantilla de Mecha]] (nueva, `tipo: mecha`) — pero es puramente narrativa (apodo, pintura, personalidad si tiene IA), las stats del frame siguen siendo de COMP/CON. Con su [[Database - Mechas]] correspondiente.
- [[Plantilla de Sesion]] sumó `enlace_encuentro_comp_con` para linkear el Encounter armado en el GM Toolkit cuando la sesión tiene combate.
- Se creó [[Como usamos COMP-CON]] como nota de referencia única: qué contenido vive en Obsidian vs. en COMP/CON, glosario Lancer, y las fuentes de datos oficiales. Linkeada desde ambos índices.
- Se dejó anotado que un homebrew mecánico propio (frame o NPC class de BorjusCorp) se empaquetaría a futuro como LCP siguiendo el esquema de `lancer-data` — no se hizo en esta pasada, el alcance actual del módulo sigue siendo solo narrativo.

## 2026-07-28 — Colapso a vault 100% DM + split Lugar/Mision + sistema de Puntos BORCORP

El usuario paró a repensar la arquitectura de fondo: "¿tiene sentido que haya cosas para los players?". Se verificó el contenido real de las 3 notas `(Conocido)` existentes (VESTA, Kharnis, La Custodia) — estaban vacías, solo placeholders "completar después de jugar". Esa evidencia confirmó que la separación GM/Jugadores era overhead puro para un GM que juega solo: duplicaba una nota por cada NPC/lugar sin que nunca se hubiera aprovechado, porque el grupo nunca va a leer el vault directamente.

Cambios:

- **`Jugadores/` desapareció por completo.** `Glosario`, `Vision General del Setting` y la fachada pública de BorjusCorp (renombrada [[BorjusCorp - Fachada Publica]] para no confundirla con [[Estructura y Jerarquia]]) se mudaron a `GM/` — son contenido real, no descartable. Las 3 notas `(Conocido)` vacías, sus plantillas, `Indice Jugadores` y `Cronologia Conocida` se borraron sin pérdida. El patrón "nota paralela filtrada" se reemplazó por una sección opcional **"## Lo que saben los jugadores"** dentro de la misma nota de NPC/Lugar — una sola fuente de verdad. `Plantilla de Sesion` (y las sesiones 00/01 ya escritas) fundieron el viejo checklist "actualizar Jugadores" en una única sección "Después de jugar" con Recap + Checklist.
- **Se separó "Planeta-Mision" en dos entidades**: [[Plantilla de Lugar]] (persistente — descripción, facciones locales, notas que se acumulan entre visitas) y [[Plantilla de Mision]] (puntual — gancho, objetivo, consecuencias, con un campo `lugar:` que linkea a su Lugar). Motivo: un mismo planeta puede tener varias misiones a lo largo de la campaña, sobre todo porque el hub de la campaña es la [[La Nave - BCS Custodia|Custodia]] visitando distintos puntos repetidamente. Se retrofiteó [[Kharnis]] e [[Ilsara]] como notas de Lugar nuevas, y se recortaron [[Mision 01 - Kharnis]] / [[Mision 02 - Ilsara]] para ser solo el evento puntual. `Database - Planetas y Misiones` se reemplazó por [[Database - Lugares]] + [[Database - Misiones]].
- **Se documentó el sistema de contrato de piloto** en [[Estructura y Jerarquia]] (sección "Los dos tipos de contrato de piloto"): cada PJ tiene o bien un pago grande (a él/ella y/o su familia) o una cuota de **10 Puntos BORCORP** (1 por misión exitosa) antes de poder dejar la compañía — dato del usuario, no inventado. [[Plantilla de Piloto]] sumó `tipo_contrato`, `puntos_borcorp_actual`, `puntos_borcorp_objetivo`; [[Database - Personajes (PJs)]] los muestra en la tabla.
- Se evaluó explícitamente no sumar "stats rápidas" de NPC en Obsidian — el usuario prefirió mantener las notas de NPC 100% narrativas y usar COMP/CON siempre para combate.

## Cómo usar esta bitácora

Agregar una entrada nueva (fecha + resumen) cada vez que se tome una decisión de diseño no trivial: cambiar el número de fragmentos, matar a un NPC importante fuera de sesión, redefinir el final, etc. No hace falta registrar cambios menores de redacción.
