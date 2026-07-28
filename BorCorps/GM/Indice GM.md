---
tipo: moc
---

# BorCorps — Índice GM

> Un grupo de pilotos recién licenciados descubre, contrato a contrato, que la corporación que los "emplea" en realidad los está usando para resucitar a un dios caído.

> [!danger] Todo lo que está bajo `GM/` es SOLO GM
> Regla simple: **nunca compartir pantalla en una nota dentro de la carpeta `GM/`**. Para material seguro de mostrar en mesa, usar el [[Indice Jugadores|Índice Jugadores]] y todo lo que está bajo `Jugadores/`. Ver [[Sugerencias de Organizacion (Investigacion)|Sugerencias de Organización]] para el porqué de esta separación.

## Navegación rápida (todo SOLO GM salvo que se indique lo contrario)

- [[Cronologia|Cronología]] (GM, completa) — versión de jugadores: [[Cronologia Conocida]]
- [[Estructura y Jerarquia|Estructura y Jerarquía]] — funcionamiento real de BorjusCorp
- [[Verdad Oculta (SOLO GM)]] — el objetivo real de la empresa
- [[Borhamus - El Ser|Mitología de Borhamus]], [[El Dios del Tiempo y la Muerte]], [[Los Fragmentos de Alma]], [[Ritual de Invocacion|Ritual de Invocación]]
- [[Motor de Misiones]] — la fórmula repetible detrás de cada misión de la campaña
- [[Arco 1 - El Inicio|Arco 1]] / [[Arco 2 - Las Facciones|Arco 2]] / [[Arco 3 - La Decision|Arco 3]] — los 3 arcos narrativos (más el [[Arco 0 - Examen Final (One-Shot)|Prólogo]])
- [[Ideas Sueltas]] / [[Bitacora de Cambios|Bitácora de Cambios]] — notas de trabajo del GM
- [[Como usamos COMP-CON]] — qué vive en Obsidian y qué vive en COMP/CON (léela antes de crear un NPC o una sesión con combate)

## Bases de datos (Dataview — se actualizan solas)

En vez de mantener listas a mano, cada tipo de entidad tiene una nota "Database" que arma la tabla leyendo el frontmatter (`tipo:`) de todas las notas de `GM/`. Para crear una entidad nueva, copiar su plantilla y listo — aparece sola en la tabla correspondiente:

- [[Database - NPCs]] (plantilla: [[Plantilla de NPC]])
- [[Database - Planetas y Misiones]] (plantilla: [[Plantilla de Planeta-Mision]])
- [[Database - Facciones Rivales]] (plantilla: [[_Plantilla de Faccion]])
- [[Database - Artefactos]] (plantilla: [[Plantilla de Artefacto]])
- [[Database - Sesiones]] (plantilla: [[Plantilla de Sesion]])

## Mapa de carpetas

```
GM/                 ⚠️ NUNCA compartir pantalla acá — todo plano, sin subcarpetas.
                    Cada nota se clasifica por su frontmatter `tipo:`, no por dónde vive.
                    Ver las notas "Database - *" de arriba para navegar por tipo.
Jugadores/          ✅ Seguro de compartir pantalla siempre — ver [[Indice Jugadores]]
                    También plano, mismo criterio de `tipo:` + notas "Database - *".
```

*(Hasta el 2026-07-28 esto estaba dividido en 10 subcarpetas numeradas dentro de `GM/` y 6 dentro de `Jugadores/`. Se aplanó todo — ver [[Bitacora de Cambios|Bitácora de Cambios]] para el porqué.)*

## Cómo funciona la campaña, en una frase

Cada sesión es una misión generada con el [[Motor de Misiones]] (conseguir una gema/artefacto, o información de una). El GM decide libremente cuándo pasar de arco según los disparadores documentados en cada nota de arco — no hay número fijo de misiones ni de sesiones. Ver [[Linea de Progresion (LL por sesion)|Línea de Progresión]] para la escala orientativa completa.

## Cómo se conectan GM y Jugadores

Cada nota GM con contraparte de jugadores tiene una línea **`Nota de jugadores:`** cerca del principio, ej. en [[VESTA - IA Capitana de la Custodia]] → [[VESTA (Conocido)]]. La convención de nombres es siempre la misma: nota GM con nombre normal, nota de jugadores con el sufijo `(Conocido)`. El flujo después de cada sesión:

1. Jugar con la nota de preparación (copiada de [[Plantilla de Sesion]], ver [[Database - Sesiones]]).
2. Escribir la Bitácora de esa sesión en `Jugadores/` (plantilla: [[_Plantilla de Bitacora de Sesion]], ver [[Database - Bitacora de Sesiones]]).
3. Crear o actualizar los `(Conocido)` de cualquier NPC/lugar nuevo mencionado — solo con lo que se reveló en mesa, nunca con la verdad completa.

Detalle completo del mecanismo y de por qué se armó así: [[Sugerencias de Organizacion (Investigacion)|Sugerencias de Organización]].

## ⚠️ Notas más sensibles dentro de GM (spoilers del final de campaña)

Todo `GM/` es spoiler por definición, pero estas son las de mayor impacto si se filtran por accidente:

- [[Verdad Oculta (SOLO GM)]]
- [[Borhamus - El Ser]]
- [[El Dios del Tiempo y la Muerte]]
- [[Ritual de Invocacion|Ritual de Invocación]]
- [[VESTA - IA Capitana de la Custodia]] — su posible giro a hostil

## Progreso de sesiones

*(completar a medida que se juega — fecha real, no fecha en el juego. El arco no se pre-asigna por número de sesión, se completa con lo que efectivamente se jugó — ver disparadores en [[Linea de Progresion (LL por sesion)|Línea de Progresión]])*

| # | Fecha | Arco | Título / resumen breve | LL alcanzado | Notas |
|---|---|---|---|---|---|
| 00 | | Prólogo | [[Sesion 00 - Examen Final]] | LL0→1 | |
| 01 | | Arco 1 | [[Sesion 01 - Primera Mision]] — [[Mision 01 - Kharnis]] | | |
| 02 | | | | | |
| 03 | | | | | |
| 04 | | | | | |
| 05 | | | | | |

*(agregar filas a medida que se juega — no hace falta completar todas de antemano)*

## Supuestos de worldbuilding (editables)

Este vault avanza con supuestos razonables donde el pedido original no especificaba algo. Todos estos son ganchos, no reglas fijas — cambialos libremente:

- La campaña ocurre en un sistema estelar aislado del resto del setting de Lancer, conectado por una única ruta NHP conocida ("el Corredor"), lo que le da a BorjusCorp control casi monopólico sobre quién entra y sale.
- BorjusCorp es una corporación de tamaño medio-grande, no una megacorp a escala de las Ocho Grandes de Lancer — más creíble como "empresa regional turbia" que como imperio galáctico.
- El grupo de PJs se conoció en la academia de pilotos de BorjusCorp (ver [[Sesion 00 - Examen Final]]).

## Para completar en la próxima sesión de trabajo

- [ ] Nombres y apariencia final de los NPCs en [[NPCs Clave de la Empresa]] y [[NPCs Recurrentes]].
- [ ] NPCs concretos de cada facción rival (líderes, recurrentes, enemigos fuertes) — ver la sección "NPCs (para completar más adelante)" en [[Custodios del Silencio]], [[Hijos del Alba Oscura]] y [[El Gremio de la Cosecha]].
- [ ] Completar [[Registro de Fragmentos (Tracker)]] con el resto de los planetas/misiones reales (Fragmentos 1 y 2 ya definidos: [[Mision 01 - Kharnis]], [[Mision 02 - Ilsara]]).
- [ ] Crear las notas de personajes en `Jugadores/` (plantilla [[Plantilla de Piloto]], ver [[Database - Personajes (PJs)]]) una vez que el grupo tenga fichas.
- [ ] Definir en COMP/CON las estadísticas placeholder marcadas como `[Definir en COMP/CON: ...]`.
- [ ] Después de jugar la Sesión 0/1: completar [[VESTA (Conocido)]] y [[Kharnis (Conocido)]] con lo que realmente pasó en mesa.
