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

## 2026-07-28 — De carpeta única a 10 carpetas por tipo de entidad + Bitácora de Campaña

Al empezar a pensar en la práctica cómo iba a usar el vault, el usuario pidió volver a tener ALGO de carpetas — no las 17 subcarpetas numeradas de antes, pero tampoco una sola carpeta plana con 47 archivos mezclados. Se armaron y confirmaron 3 decisiones de diseño en conjunto:

1. **10 carpetas por tipo de entidad, un solo nivel, sin numeración**: `Sesiones/`, `NPCs/`, `Lugares/`, `Misiones/`, `Facciones/`, `Personajes/`, `Artefactos/`, `Mundo/`, `Campana/`, `Bitacora de Campana/`. El wrapper `GM/` se eliminó — como el vault es 100% del GM, ya no cumplía ninguna función distinguir nada de "GM/". Cada Database ahora apunta `FROM` a su carpeta específica en vez de `FROM "GM"`. Las sesiones 00/01 se renombraron a `00 - Examen Final.md` / `01 - Primera Mision.md` (sin el prefijo "Sesion", ya redundante dentro de la carpeta `Sesiones/`) — se actualizaron todos los wikilinks que las nombraban por el nombre viejo.
2. **Sub-lugares dentro de un planeta van por nomenclatura + link, no por subcarpeta**: `"Planeta - Sublugar.md"` con un campo `planeta:` en el frontmatter y una línea de vuelta al planeta — se descartó la opción de subcarpeta-por-planeta porque reintroducía profundidad de carpetas que el usuario específicamente quería evitar, y Obsidian ya resuelve la navegación "ir y volver" con wikilinks sin necesitar jerarquía de archivos real.
3. **Se creó `Bitacora de Campana/`** con un file semilla (`Bitacora de Campana.md`) — memoria narrativa en prosa de lo que pasó en cada sesión, separada por `---`, distinta de la `Bitacora de Cambios` (esa es meta/diseño del vault). El usuario prefirió esto explícitamente por sobre reusar `Database - Sesiones` + el Registro de Fragmentos, aunque ya cubrían buena parte de lo mismo — quedó como carpeta flexible: un solo file por ahora, con la opción abierta de partirlo en un file por sesión más adelante si se vuelve incómodo.

También se le sumó un resumen Dataview (`GROUP BY estado_fragmento`) arriba de la tabla manual del [[Registro de Fragmentos (Tracker)]], para tener el conteo de gemas por estado sin mantenerlo a mano dos veces. Se reclasificó [[La Nave - BCS Custodia]] de `tipo: mundo` a `tipo: lugar` y se movió a `Lugares/`, ya que es el hub móvil de la campaña.

## 2026-07-28 — Renombre de Mundo/ a Ambientacion/ y campo categoria_lugar

El usuario notó una colisión conceptual: la carpeta `Mundo/` (Cronología, Glosario, Visión del Setting) sonaba como si ahí debieran vivir los planetas, cuando en realidad los planetas ya vivían en `Lugares/` (Kharnis, Ilsara, La Nave). Se confirmó que `Lugares/` ya hacía exactamente lo que el usuario pedía — mundos, sub-lugares dentro de un mundo, y lugares independientes como la nave, todo junto y linkeado — así que no hubo que tocar esa carpeta. Se renombró `Mundo/` a `Ambientacion/` (más `tipo: mundo` → `tipo: ambientacion` en sus 3 notas) para eliminar la ambigüedad.

Además, a pedido del usuario, se agregó el campo `categoria_lugar` (`Planeta` o `Lugar`) a [[Plantilla de Lugar]] como columna visible en [[Database - Lugares]] — antes la distinción "es un mundo vs. cuelga de un mundo" era implícita (campo `pertenece_a_mundo` vacío o no), ahora es explícita y se lee de un vistazo en la tabla. `pertenece_a_mundo` se mantiene, pero solo se completa cuando `categoria_lugar: Lugar` Y pertenece a un planeta específico (no aplica a lugares independientes como la Custodia).

## 2026-07-28 — Planeta como tipo propio, separado de Lugar

Corrección de modelo, a pedido del usuario: `categoria_lugar: Planeta | Lugar` (agregado unas horas antes en esta misma sesión) forzaba dos conceptos distintos dentro de un único `tipo: lugar`. Un planeta *contiene* lugares — no es una variante de lugar, es su propio tipo de entidad. Se corrigió:

- **`tipo: planeta`** (nueva [[Plantilla de Planeta]]) para mundos enteros — [[Kharnis]] e [[Ilsara]] pasaron de `tipo: lugar` + `categoria_lugar: Planeta` a directamente `tipo: planeta`, sin ese campo.
- **`tipo: lugar`** ([[Plantilla de Lugar]], simplificada) para todo lo que no es un planeta entero: sub-lugares puntuales dentro de uno (campo `planeta:` completo) o lugares independientes como [[La Nave - BCS Custodia]] (campo `planeta:` vacío). El campo se renombró de `pertenece_a_mundo` a simplemente `planeta` — más directo ahora que "planeta" es un tipo con nombre propio.
- [[Database - Lugares]] se dividió en [[Database - Planetas]] (`tipo: planeta`) y [[Database - Lugares]] (`tipo: lugar`, ahora con columna "Planeta" para ver de un vistazo si es independiente o cuelga de uno) — mismo patrón de "una Database por tipo" que ya se usa en el resto del vault.
- Ambas siguen viviendo en la carpeta `Lugares/` sin separarse en carpetas — la corrección fue de `tipo:`, no de organización de carpetas.
- Se sacó el campo `region` de ambas plantillas y de las 3 notas existentes — se había agregado sin un uso concreto (solo había una región, "El Corredor") y el usuario lo marcó como complejidad sin justificar. Regla para adelante: no agregar un campo de frontmatter sin poder explicar para qué sirve todavía.

## Cómo usar esta bitácora

Agregar una entrada nueva (fecha + resumen) cada vez que se tome una decisión de diseño no trivial: cambiar el número de fragmentos, matar a un NPC importante fuera de sesión, redefinir el final, etc. No hace falta registrar cambios menores de redacción.
