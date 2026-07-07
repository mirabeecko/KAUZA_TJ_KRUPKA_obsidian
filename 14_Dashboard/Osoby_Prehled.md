---
typ: prehled
nazev: Přehled osob
tagy:
  - prehled
  - osoby
---

# Přehled osob

## Všechny osoby

```dataview
TABLE id, cele_jmeno, role, organizace, relevance, stav
FROM "01_Osoby"
WHERE typ = "osoba"
SORT relevance DESC, prijmeni ASC
```

## Osoby bez vazby na organizaci

```dataview
TABLE id, cele_jmeno, role
FROM "01_Osoby"
WHERE typ = "osoba" AND !organizace
SORT prijmeni ASC
```

## Osoby podle organizace

```dataview
TABLE id, cele_jmeno, role, relevance
FROM "01_Osoby"
WHERE typ = "osoba"
GROUP BY organizace
```

## Důkazy podle osob

```dataview
TABLE id, datum, typ, zdroj
FROM "04_Dukazy"
WHERE typ = "dukaz"
GROUP BY osoby
SORT datum DESC
```

## Tvrzení podle osob

```dataview
TABLE id, text_tvrzeni, stav
FROM "07_Tvrzeni"
WHERE typ = "tvrzeni"
GROUP BY osoby
```
