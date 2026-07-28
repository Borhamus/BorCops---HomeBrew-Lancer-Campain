---
tipo: database
---

# Base de datos — Planetas

> [!info] Esta tabla se arma sola
> Generada con Dataview a partir de `tipo: planeta`. Para agregar uno nuevo: copiar [[Plantilla de Planeta]]. Un planeta puede tener varias misiones a lo largo de la campaña — ver [[Database - Misiones]] y filtrar por su campo `lugar`.

```dataview
LIST
FROM "Lugares"
WHERE tipo = "planeta" AND !contains(file.name, "Plantilla")
SORT file.name ASC
```

## Ver también

- [[Plantilla de Planeta]]
- [[Database - Lugares]] — sub-lugares y lugares independientes (no planetas enteros)
- [[Database - Misiones]]
