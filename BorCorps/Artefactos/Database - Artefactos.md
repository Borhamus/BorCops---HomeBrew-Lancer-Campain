---
tipo: database
---

# Base de datos — Artefactos

> [!info] Esta tabla se arma sola
> Generada con Dataview a partir de `tipo: artefacto`. Para agregar uno nuevo: copiar [[Plantilla de Artefacto]] y completar el frontmatter (`fragmento_numero`, `estado`, `ubicacion`).

```dataview
TABLE
  fragmento_numero AS "Fragmento #",
  estado AS "Estado",
  ubicacion AS "Ubicación"
FROM "Artefactos"
WHERE tipo = "artefacto" AND !contains(file.name, "Plantilla")
SORT fragmento_numero ASC
```

## Ver también

- [[Plantilla de Artefacto]]
- [[Registro de Fragmentos (Tracker)]] 
