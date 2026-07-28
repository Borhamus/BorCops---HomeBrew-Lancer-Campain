---
tipo: database
---

# Base de datos — Planetas y Misiones

> [!info] Esta tabla se arma sola
> Generada con Dataview a partir de `tipo: planeta-mision`. Para agregar una misión nueva: copiar [[Plantilla de Planeta-Mision]] y completar el frontmatter (`arco`, `estado_fragmento`).

```dataview
TABLE
  arco AS "Arco",
  estado_fragmento AS "Estado del fragmento"
FROM "GM"
WHERE tipo = "planeta-mision" AND !contains(file.name, "Plantilla")
SORT file.name ASC
```

## Ver también

- [[Plantilla de Planeta-Mision]]
- [[Registro de Fragmentos (Tracker)]] — estado narrativo de los 7 fragmentos (esta tabla es el índice de notas, esa es el tracker de trama)
- [[Database - Lugares Conocidos]] — la versión filtrada, del lado Jugadores
