---
tipo: database
---

# Base de datos — Personajes (PJs)

> [!info] Esta tabla se arma sola
> Generada con Dataview a partir de `tipo: pj`. Para crear la ficha de un piloto nuevo: copiar [[Plantilla de Piloto]] y completar el frontmatter (`jugador`, `LL_actual`). Esto es solo trasfondo narrativo — las estadísticas mecánicas del piloto y su mecha se llevan en COMP/CON, no acá.

```dataview
TABLE
  jugador AS "Jugador",
  LL_actual AS "LL actual",
  tipo_contrato AS "Contrato",
  puntos_borcorp_actual AS "Puntos BORCORP"
FROM "GM"
WHERE tipo = "pj" AND !contains(file.name, "Plantilla")
SORT file.name ASC
```

## Ver también

- [[Plantilla de Piloto]]
- [[Estructura y Jerarquia]] — sección "Los dos tipos de contrato de piloto"
- [COMP/CON](https://compcon.app) — creador de fichas oficial de Lancer, para stats de piloto y mecha
