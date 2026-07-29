---
tipo: tracker
spoiler: true
---

> [!danger] SOLO GM — spoilers de trama
> Esta tabla es el estado real de los 7 fragmentos. No mostrar a los jugadores.

# Registro de Fragmentos (Tracker)

Ver [[Los Fragmentos de Alma]] para la explicación conceptual de qué es un fragmento y qué significa cada estado.

## Resumen (se arma solo, lee `estado_fragmento` de cada Misión)

```dataview
TABLE WITHOUT ID estado_fragmento AS "Estado", length(rows) AS "Cantidad"
FROM "Misiones"
WHERE tipo = "mision"
GROUP BY estado_fragmento
```

## Detalle (mantener a mano — quién la tiene, notas de contexto)

| #   | Planeta / Misión | Estado      | Recuperado por | Notas                                                                 |
| --- | ---------------- | ----------- | -------------- | --------------------------------------------------------------------- |
| 1   | [[Mision 01 - Kharnis]] | contenido   | —              | Pendiente de sesión 1. Si la extracción sale bien, pasa a `recuperado por BorCorp` — actualizar tras jugarla. |
| 2   | *(a definir)*    | contenido   | —              |                                                                       |
| 3   | *(a definir)*    | contenido   | —              |                                                                       |
| 4   | *(a definir)*    | desconocido | —              |                                                                       |
| 5   | *(a definir)*    | desconocido | —              |                                                                       |
| 6   | *(a definir)*    | contenido   | —              | Buen candidato: un sitio ligado a alguno de [[Los 12 Dioses de la Antigüedad|Los Doce]] |
| 7   | *(a definir)*    | contenido   | —              |                                                                       |

## Estados válidos

`contenido` · `roto` · `recuperado por BorCorp` · `recuperado por los jugadores` · `desconocido`

## Cómo usar esta tabla

- Cada fila debería eventualmente linkear a una nota de Lugar y a su [[Plantilla de Mision|Mision]] correspondiente (columna "Planeta / Misión") y, cuando exista, a su nota de artefacto (usar la [[Plantilla de Artefacto]]).
- Actualizar el estado apenas cambie en sesión — es el mejor termómetro de qué tan cerca está el Consejo Fundador de completar el [[Ritual de Invocacion|Ritual de Invocación]] (referencia: necesitan al menos 5 de 7, ver esa nota).

## Ver también (todos SOLO GM salvo la plantilla)

- [[Los Fragmentos de Alma]]
- [[Ritual de Invocacion|Ritual de Invocación]]
- [[Plantilla de Artefacto]]
