---
typ: prehled
nazev: Přehled dokumentů
tagy:
  - prehled
  - dokumenty
---

# Přehled dokumentů

## Všechny dokumenty

```dataview
TABLE id, datum, kategorie, nazev, autor, vydavatel
FROM "05_Dokumenty"
WHERE typ = "dokument"
SORT datum DESC
```

## Dokumenty podle kategorie

```dataview
TABLE id, datum, nazev, autor
FROM "05_Dokumenty"
WHERE typ = "dokument"
GROUP BY kategorie
SORT datum DESC
```

## Dokumenty podle roku

```dataview
TABLE id, datum, kategorie, nazev
FROM "05_Dokumenty"
WHERE typ = "dokument"
GROUP BY dateformat(datum, "yyyy")
SORT datum DESC
```

## Dokumenty bez vazeb

```dataview
TABLE id, datum, nazev, kategorie
FROM "05_Dokumenty"
WHERE !osoby AND !organizace AND !udalosti
SORT datum DESC
```

## Dokumenty bez fyzického souboru

```dataview
TABLE id, datum, nazev, kategorie
FROM "05_Dokumenty"
WHERE !soubor
SORT datum DESC
```
