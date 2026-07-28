---
tipo: database
---

# Base de datos — Lugares

> [!info] Esta tabla se arma sola
> Generada con Dataview a partir de `tipo: lugar`. Para agregar uno nuevo: copiar [[Plantilla de Lugar]] y completar el frontmatter (`categoria_lugar`, `region`, `pertenece_a_mundo` si es un Lugar que cuelga de un Planeta). Un lugar puede tener varias misiones a lo largo de la campaña — ver [[Database - Misiones]] y filtrar por su campo `lugar`.

```dataview
TABLE
  categoria_lugar AS "Categoría",
  region AS "Región",
  pertenece_a_mundo AS "Pertenece a"
FROM "Lugares"
WHERE tipo = "lugar" AND !contains(file.name, "Plantilla")
SORT categoria_lugar ASC, file.name ASC
```

## Ver también

- [[Plantilla de Lugar]]
- [[Database - Misiones]]
