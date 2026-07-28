---
tipo: database
---

# Base de datos — Lugares y Misiones Conocidos

> [!info] Esta tabla se arma sola
> Generada con Dataview a partir de `tipo: conocido-lugar`. Para agregar uno nuevo: copiar [[_Plantilla de Lugar Conocido]] y completar el frontmatter (`actualizado_hasta_sesion`).

```dataview
TABLE actualizado_hasta_sesion AS "Actualizado hasta sesión"
FROM "Jugadores"
WHERE tipo = "conocido-lugar" AND !contains(file.name, "Plantilla")
SORT file.name ASC
```

## Ver también

- [[_Plantilla de Lugar Conocido]]
