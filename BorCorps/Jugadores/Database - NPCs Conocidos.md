---
tipo: database
---

# Base de datos — NPCs Conocidos

> [!info] Esta tabla se arma sola
> Generada con Dataview a partir de `tipo: conocido-npc`. Para agregar uno nuevo: copiar [[_Plantilla de NPC Conocido]] y completar el frontmatter (`actualizado_hasta_sesion`).

```dataview
TABLE actualizado_hasta_sesion AS "Actualizado hasta sesión"
FROM "Jugadores"
WHERE tipo = "conocido-npc" AND !contains(file.name, "Plantilla")
SORT file.name ASC
```

## Ver también

- [[_Plantilla de NPC Conocido]]
