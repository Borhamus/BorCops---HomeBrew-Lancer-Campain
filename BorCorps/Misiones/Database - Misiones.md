---
tipo: database
---

# Base de datos — Misiones

> [!info] Esta tabla se arma sola
> Generada con Dataview a partir de `tipo: mision`. Para agregar una nueva: copiar [[Plantilla de Mision]] y completar el frontmatter (`lugar`, `arco`, `estado_fragmento`).

```dataview
TABLE
  lugar AS "Lugar",
  arco AS "Arco",
  estado_fragmento AS "Estado del fragmento"
FROM "Misiones"
WHERE tipo = "mision" AND !contains(file.name, "Plantilla")
SORT file.name ASC
```

## Ver también

- [[Plantilla de Mision]]
- [[Database - Lugares]]
- [[Registro de Fragmentos (Tracker)]] — estado narrativo de los 7 fragmentos (esta tabla es el índice de notas, esa es el tracker de trama)
