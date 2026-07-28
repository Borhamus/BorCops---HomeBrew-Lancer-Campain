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

## Cómo usar esta bitácora

Agregar una entrada nueva (fecha + resumen) cada vez que se tome una decisión de diseño no trivial: cambiar el número de fragmentos, matar a un NPC importante fuera de sesión, redefinir el final, etc. No hace falta registrar cambios menores de redacción.
