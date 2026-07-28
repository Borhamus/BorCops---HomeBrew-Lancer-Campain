---
tipo: database
---

# Base de datos — Sesiones (preparación GM)

> [!info] Esta tabla se arma sola
> Generada con Dataview a partir de `tipo: sesion`. Para preparar una sesión nueva: copiar [[Plantilla de Sesion]] y completar el frontmatter (`numero`, `arco`, `fecha_real`, `fecha_en_juego`).

```dataview
TABLE
  numero AS "#",
  arco AS "Arco",
  fecha_real AS "Fecha real",
  fecha_en_juego AS "Fecha en juego"
FROM "GM"
WHERE tipo = "sesion" AND !contains(file.name, "Plantilla")
SORT numero ASC
```

## Ver también

- [[Plantilla de Sesion]] — incluye la sección de recap post-sesión
