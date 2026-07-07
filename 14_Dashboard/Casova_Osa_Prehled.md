---
typ: prehled
nazev: Chronologická časová osa
tagy:
  - prehled
  - casova_osa
cssclasses:
---

# Chronologická časová osa

> [!NOTE] Automaticky generovaná časová osa ze všech událostí, dokumentů a důkazů

## Události chronologicky

```dataview
TABLE datum, nazev, misto, osoby, organizace
FROM "03_Udalosti"
WHERE typ = "udalost"
SORT datum ASC
```

## Dokumenty chronologicky

```dataview
TABLE datum, kategorie, nazev, autor, vydavatel
FROM "05_Dokumenty"
WHERE typ = "dokument"
SORT datum ASC
```

## Důkazy chronologicky

```dataview
TABLE datum, typ, zdroj, osoby, stav_dukazu
FROM "04_Dukazy"
WHERE typ = "dukaz"
SORT datum ASC
```

## Vše chronologicky (kombinovaný pohled)

```dataview
TABLE datum, typ, file.name, popis
FROM "03_Udalosti", "04_Dukazy", "05_Dokumenty"
SORT datum ASC
```

## Dokumenty podle roku

```dataview
TABLE id, datum, kategorie, nazev
FROM "05_Dokumenty"
WHERE typ = "dokument"
GROUP BY dateformat(datum, "yyyy")
SORT datum ASC
```
