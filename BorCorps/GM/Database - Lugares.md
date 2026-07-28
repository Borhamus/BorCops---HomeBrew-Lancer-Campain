---
tipo: database
---

# Base de datos — Lugares

> [!info] Esta tabla se arma sola
> Generada con Dataview a partir de `tipo: lugar`. Para agregar uno nuevo: copiar [[Plantilla de Lugar]] y completar el frontmatter (`region`). Un lugar puede tener varias misiones a lo largo de la campaña — ver [[Database - Misiones]] y filtrar por su campo `lugar`.

```dataview
TABLE region AS "Región"
FROM "GM"
WHERE tipo = "lugar" AND !contains(file.name, "Plantilla")
SORT file.name ASC
```

## Ver también

- [[Plantilla de Lugar]]
- [[Database - Misiones]]
