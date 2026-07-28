---
tipo: database
---

# Base de datos — Facciones Rivales

> [!info] Esta tabla se arma sola
> Generada con Dataview a partir de `tipo: faccion-rival`. Para agregar una facción nueva: copiar [[_Plantilla de Faccion]] y completar el frontmatter (`metodo`, `tono`).

```dataview
TABLE
  metodo AS "Método",
  tono AS "Tono"
FROM "GM"
WHERE tipo = "faccion-rival" AND !contains(file.name, "Plantilla")
SORT file.name ASC
```

## Ver también

- [[_Plantilla de Faccion]]
- [[Arco 2 - Las Facciones]]
