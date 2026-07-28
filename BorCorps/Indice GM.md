---
tipo: moc
---

# BorCorps — Índice GM

> Un grupo de pilotos recién licenciados descubre, contrato a contrato, que la corporación que los "emplea" en realidad los está usando para resucitar a un dios caído.

> [!info] Este vault es 100% tuyo como GM
> No hay una versión "para jugadores" — nada acá está pensado para compartir pantalla directamente. Si algo es especialmente sensible (spoilers del final), usá el frontmatter `spoiler: true` como marca visual, y contále al grupo lo que corresponda en mesa con tus propias palabras, no leyendo la nota.

## Navegación rápida

- [[Cronologia|Cronología]]
- [[Estructura y Jerarquia|Estructura y Jerarquía]] — funcionamiento real de BorjusCorp, incluido el sistema de contratos (Pago vs. Puntos BORCORP)
- [[Verdad Oculta (SOLO GM)]] — el objetivo real de la empresa
- [[Borhamus - El Ser|Mitología de Borhamus]], [[El Dios del Tiempo y la Muerte]], [[Los Fragmentos de Alma]], [[Ritual de Invocacion|Ritual de Invocación]]
- [[Motor de Misiones]] — la fórmula repetible detrás de cada misión de la campaña
- [[Arco 1 - El Inicio|Arco 1]] / [[Arco 2 - Las Facciones|Arco 2]] / [[Arco 3 - La Decision|Arco 3]] — los 3 arcos narrativos (más el [[Arco 0 - Examen Final (One-Shot)|Prólogo]])
- [[Ideas Sueltas]] / [[Bitacora de Cambios|Bitácora de Cambios]] — notas de trabajo sobre el vault en sí
- [[Bitacora de Campana/Bitacora de Campana|Bitácora de Campaña]] — memoria narrativa de lo que pasó en mesa, sesión a sesión
- [[Como usamos COMP-CON]] — qué vive en Obsidian y qué vive en COMP/CON (léela antes de crear un NPC o una sesión con combate)

## Mapa de carpetas

```
Sesiones/    Prep + recap de cada sesión (Plantilla de Sesion)
NPCs/        Un file por NPC (Plantilla de NPC)
Lugares/     Planetas y la Custodia — persistente (Plantilla de Lugar)
Misiones/    Eventos puntuales, cada uno linkea a su Lugar (Plantilla de Mision)
Facciones/   Las 3 facciones rivales (_Plantilla de Faccion)
Personajes/  Pilotos (PJs) y sus mechas — narrativa, stats en COMP/CON
Artefactos/  Los 7 fragmentos + el tracker (Plantilla de Artefacto)
Ambientacion/  Lore de referencia (no son lugares): Cronología, Glosario, Visión del Setting
Campana/     Arcos, Motor de Misiones, mitología de Borhamus, estructura real de BorjusCorp
Bitacora de Campana/   Memoria narrativa acumulada de la campaña
```

Más [[Indice GM]], [[Bitacora de Cambios|Bitácora de Cambios]], [[Ideas Sueltas]], [[Como usamos COMP-CON]] y [[Sugerencias de Organizacion (Investigacion)|Sugerencias de Organización]] sueltas en la raíz — son notas de gestión del vault, no de campaña.

## Bases de datos (Dataview — se actualizan solas)

Cada carpeta de entidad tiene su nota "Database" que arma la tabla leyendo el frontmatter (`tipo:`) de esa carpeta. Para crear una entidad nueva, copiar su plantilla y listo — aparece sola en la tabla correspondiente:

- [[Database - NPCs]] (`NPCs/`, plantilla: [[Plantilla de NPC]])
- [[Database - Lugares]] (`Lugares/`, plantilla: [[Plantilla de Lugar]])
- [[Database - Misiones]] (`Misiones/`, plantilla: [[Plantilla de Mision]])
- [[Database - Facciones Rivales]] (`Facciones/`, plantilla: [[_Plantilla de Faccion]])
- [[Database - Artefactos]] (`Artefactos/`, plantilla: [[Plantilla de Artefacto]])
- [[Database - Sesiones]] (`Sesiones/`, plantilla: [[Plantilla de Sesion]])
- [[Database - Personajes (PJs)]] (`Personajes/`, plantilla: [[Plantilla de Piloto]])
- [[Database - Mechas]] (`Personajes/`, plantilla: [[Plantilla de Mecha]])

*(Hasta el 2026-07-28 esto pasó por dos formas: 17 subcarpetas numeradas divididas entre `GM/`+`Jugadores/`, y después una sola carpeta plana. Se terminó de asentar en estas 10 carpetas por tipo de entidad — ver [[Bitacora de Cambios|Bitácora de Cambios]] para el porqué de cada paso.)*

## Mundos, lugares independientes, y sub-lugares — todo en `Lugares/`

Un mundo/planeta es un tipo de lugar más — por eso todos conviven en la misma carpeta plana, sin una carpeta "Mundos" separada. La distinción rápida es el campo `categoria_lugar`, visible como columna en [[Database - Lugares]]:

- **`categoria_lugar: Planeta`** — un mundo en sí mismo (ej. [[Kharnis]], [[Ilsara]]).
- **`categoria_lugar: Lugar`** — cualquier otra cosa: un lugar independiente que no es un planeta (ej. [[La Nave - BCS Custodia|la Custodia]], el hub móvil), o un sub-lugar dentro de un planeta (ej. un obelisco puntual dentro de Kharnis).

Cuando un `Lugar` sí pertenece a un `Planeta` específico (no es independiente como la Custodia), completar `pertenece_a_mundo: "[[Kharnis]]"` en su frontmatter — así el GM siempre puede saltar directo ahí con un click. Convención de nombre para sub-lugares: `"Planeta - Sublugar.md"` (ej. `Kharnis - Obelisco.md`) — se ordenan solos alfabéticamente junto a su planeta en el explorador de archivos, sin necesitar ninguna subcarpeta.

## Cómo funciona la campaña, en una frase

Cada sesión es una misión generada con el [[Motor de Misiones]] (conseguir una gema/artefacto, o información de una). El GM decide libremente cuándo pasar de arco según los disparadores documentados en cada nota de arco — no hay número fijo de misiones ni de sesiones. Ver [[Linea de Progresion (LL por sesion)|Línea de Progresión]] para la escala orientativa completa.

## Cómo ir revelando información en mesa

Este vault no tiene una nota paralela "filtrada" por cada NPC/lugar — la verdad completa y lo que el grupo sabe conviven en la misma nota. El flujo después de cada sesión:

1. Jugar con la nota de preparación (copiada de [[Plantilla de Sesion]], ver [[Database - Sesiones]]) y completar su sección "Recap".
2. En cada NPC, Lugar o Misión que haya salido en mesa, agregar/actualizar su sección **"Lo que saben los jugadores"** — solo con lo que efectivamente se reveló, nunca con la verdad completa de arriba.
3. Actualizar la fila correspondiente en la tabla de "Progreso de sesiones" más abajo.

## ⚠️ Notas más sensibles (spoilers del final de campaña)

Estas son las de mayor impacto si se te escapa algo en mesa sin querer:

- [[Verdad Oculta (SOLO GM)]]
- [[Borhamus - El Ser]]
- [[El Dios del Tiempo y la Muerte]]
- [[Ritual de Invocacion|Ritual de Invocación]]
- [[VESTA - IA Capitana de la Custodia]] — su posible giro a hostil

## Progreso de sesiones

*(completar a medida que se juega — fecha real, no fecha en el juego. El arco no se pre-asigna por número de sesión, se completa con lo que efectivamente se jugó — ver disparadores en [[Linea de Progresion (LL por sesion)|Línea de Progresión]])*

| # | Fecha | Arco | Título / resumen breve | LL alcanzado | Notas |
|---|---|---|---|---|---|
| 00 | | Prólogo | [[00 - Examen Final]] | LL0→1 | |
| 01 | | Arco 1 | [[01 - Primera Mision]] — [[Mision 01 - Kharnis]] | | |
| 02 | | | | | |
| 03 | | | | | |
| 04 | | | | | |
| 05 | | | | | |

*(agregar filas a medida que se juega — no hace falta completar todas de antemano)*

## Supuestos de worldbuilding (editables)

Este vault avanza con supuestos razonables donde el pedido original no especificaba algo. Todos estos son ganchos, no reglas fijas — cambialos libremente:

- La campaña ocurre en un sistema estelar aislado del resto del setting de Lancer, conectado por una única ruta NHP conocida ("el Corredor"), lo que le da a BorjusCorp control casi monopólico sobre quién entra y sale.
- BorjusCorp es una corporación de tamaño medio-grande, no una megacorp a escala de las Ocho Grandes de Lancer — más creíble como "empresa regional turbia" que como imperio galáctico.
- El grupo de PJs se conoció en la academia de pilotos de BorjusCorp (ver [[00 - Examen Final]]).
- Cada PJ tiene su propio tipo de contrato con BorjusCorp — pago grande o cuota de 10 Puntos BORCORP — ver [[Estructura y Jerarquia]].

## Para completar en la próxima sesión de trabajo

- [ ] Nombres y apariencia final de los NPCs en [[NPCs Clave de la Empresa]] y [[NPCs Recurrentes]].
- [ ] NPCs concretos de cada facción rival (líderes, recurrentes, enemigos fuertes) — ver la sección "NPCs (para completar más adelante)" en [[Custodios del Silencio]], [[Hijos del Alba Oscura]] y [[El Gremio de la Cosecha]].
- [ ] Completar [[Registro de Fragmentos (Tracker)]] con el resto de los lugares/misiones reales (Fragmentos 1 y 2 ya definidos: [[Mision 01 - Kharnis]], [[Mision 02 - Ilsara]]).
- [ ] Crear las notas de personajes con [[Plantilla de Piloto]] (ver [[Database - Personajes (PJs)]]) una vez que el grupo tenga fichas — definir `tipo_contrato` de cada uno.
- [ ] Definir en COMP/CON las estadísticas placeholder marcadas como `[Definir en COMP/CON: ...]`.
- [ ] Después de jugar la Sesión 0/1: completar "Lo que saben los jugadores" en [[VESTA - IA Capitana de la Custodia]], [[Kharnis]] y [[Mision 01 - Kharnis]] con lo que realmente pasó en mesa.
