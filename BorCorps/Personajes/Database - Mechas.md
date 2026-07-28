---
tipo: database
---

# Base de datos — Mechas

> [!info] Esta tabla se arma sola
> Generada con Dataview a partir de `tipo: mecha`. Para agregar uno nuevo: copiar [[Plantilla de Mecha]] y completar el frontmatter (`piloto`, `frame`, `fabricante`). Las stats reales del frame viven en COMP/CON — ver [[Como usamos COMP-CON]].

```dataview
TABLE
  piloto AS "Piloto",
  frame AS "Frame",
  fabricante AS "Fabricante"
FROM "Personajes"
WHERE tipo = "mecha" AND !contains(file.name, "Plantilla")
SORT file.name ASC
```

## Ver también

- [[Plantilla de Mecha]]
- [[Como usamos COMP-CON]]
