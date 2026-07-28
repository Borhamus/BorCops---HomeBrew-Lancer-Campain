---
tipo: database
---

# Base de datos — Lugares

> [!info] Esta tabla se arma sola
> Generada con Dataview a partir de `tipo: lugar` (sub-lugares dentro de un planeta, o lugares independientes como la Custodia — para planetas enteros ver [[Database - Planetas]]). Para agregar uno nuevo: copiar [[Plantilla de Lugar]] y completar el frontmatter (`planeta` si cuelga de uno).

```dataview
TABLE planeta AS "Planeta"
FROM "Lugares"
WHERE tipo = "lugar" AND !contains(file.name, "Plantilla")
SORT file.name ASC
```

*(fila con "Planeta" vacío = es un lugar independiente, como la Custodia)*

## Ver también

- [[Plantilla de Lugar]]
- [[Database - Planetas]]
