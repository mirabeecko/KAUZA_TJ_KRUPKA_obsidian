---
typ: prehled
nazev: Přehled událostí
tagy:
  - prehled
  - udalosti
---

# Přehled událostí

## Všechny události chronologicky

```dataview
TABLE id, datum, nazev, misto, osoby, organizace, stav_vysetreni
FROM "03_Udalosti"
WHERE typ = "udalost"
SORT datum ASC
```

## Neprošetřené události

```dataview
TABLE id, datum, nazev, misto, osoby
FROM "03_Udalosti"
WHERE stav_vysetreni = "neovereno"
SORT datum ASC
```

## Události bez důkazů

```dataview
TABLE id, datum, nazev, misto
FROM "03_Udalosti"
WHERE typ = "udalost" AND !dukazy
SORT datum ASC
```

## Události bez dokumentů

```dataview
TABLE id, datum, nazev, misto
FROM "03_Udalosti"
WHERE typ = "udalost" AND !dokumenty
SORT datum ASC
```

## Události podle místa

```dataview
TABLE id, datum, nazev, osoby
FROM "03_Udalosti"
WHERE typ = "udalost"
GROUP BY misto
SORT datum ASC
```
