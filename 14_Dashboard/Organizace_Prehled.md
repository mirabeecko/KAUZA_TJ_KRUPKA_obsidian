---
typ: prehled
nazev: Přehled organizací
tagy:
  - prehled
  - organizace
---

# Přehled organizací

## Všechny organizace

```dataview
TABLE id, nazev, sidlo, relevance, stav
FROM "02_Organizace"
WHERE typ = "organizace"
SORT relevance DESC, nazev ASC
```

## Organizace podle právní formy

```dataview
TABLE id, nazev, ico, relevance
FROM "02_Organizace"
WHERE typ = "organizace"
GROUP BY pravni_forma
SORT nazev ASC
```

## Nejaktivnější organizace — počet dokumentů

```dataview
TABLE id, nazev, ico
FROM "02_Organizace"
WHERE typ = "organizace"
SORT file.inlinks DESC
LIMIT 10
```

## Důkazy podle organizací

```dataview
TABLE id, datum, typ, stav_dukazu
FROM "04_Dukazy"
WHERE typ = "dukaz"
GROUP BY organizace
SORT datum DESC
```
