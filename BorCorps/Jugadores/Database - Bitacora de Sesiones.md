---
tipo: database
---

# Base de datos — Bitácora de Sesiones

> [!info] Esta tabla se arma sola
> Generada con Dataview a partir de `tipo: bitacora-sesion`. Para agregar el recap de una sesión nueva: copiar [[_Plantilla de Bitacora de Sesion]] y completar el frontmatter (`numero`, `fecha_en_juego`).

```dataview
TABLE
  numero AS "#",
  fecha_en_juego AS "Fecha en juego"
FROM "Jugadores"
WHERE tipo = "bitacora-sesion" AND !contains(file.name, "Plantilla")
SORT numero ASC
```

## Ver también

- [[_Plantilla de Bitacora de Sesion]]
- [[Database - Sesiones]] — la versión de preparación, del lado GM
