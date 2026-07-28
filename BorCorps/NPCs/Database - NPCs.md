---
tipo: database
---

# Base de datos — NPCs

> [!info] Esta tabla se arma sola
> No hace falta mantener esta lista a mano. Dataview la genera leyendo el frontmatter de cada nota con `tipo: npc` dentro de `NPCs/`. Para agregar un NPC nuevo: copiar [[Plantilla de NPC]], completar el frontmatter (`faccion`, `rol_en_trama`, `vivo`) y va a aparecer acá solo.

```dataview
TABLE
  faccion AS "Facción",
  rol_en_trama AS "Rol en trama",
  vivo AS "¿Vivo?"
FROM "NPCs"
WHERE tipo = "npc" AND !contains(file.name, "Plantilla")
SORT file.name ASC
```

## Ver también

- [[Plantilla de NPC]]
- [[NPCs Clave de la Empresa]] — análisis narrativo (qué sabe cada uno), esta tabla es solo el índice rápido
