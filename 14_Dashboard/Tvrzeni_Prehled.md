---
typ: prehled
nazev: Přehled tvrzení
tagy:
  - prehled
  - tvrzeni
---

# Přehled tvrzení

## Všechna tvrzení

```dataview
TABLE id, text_tvrzeni, tvrditel, stav, datum_tvrzeni
FROM "07_Tvrzeni"
WHERE typ = "tvrzeni"
SORT stav ASC, datum_tvrzeni DESC
```

## Neověřená tvrzení

```dataview
TABLE id, text_tvrzeni, tvrditel, datum_tvrzeni, osoby
FROM "07_Tvrzeni"
WHERE stav = "neovereno"
SORT datum_tvrzeni DESC
```

## Částečně podložená tvrzení

```dataview
TABLE id, text_tvrzeni, tvrditel, podpora_dukazy
FROM "07_Tvrzeni"
WHERE stav = "castecne_podlozeno"
```

## Podložená tvrzení

```dataview
TABLE id, text_tvrzeni, tvrditel, podpora_dukazy
FROM "07_Tvrzeni"
WHERE stav = "podlozeno"
```

## Vyvrácená tvrzení

```dataview
TABLE id, text_tvrzeni, tvrditel, vyvraceni_dukazy
FROM "07_Tvrzeni"
WHERE stav = "vyvraceno"
```

## Tvrzení bez jakýchkoliv důkazů

```dataview
TABLE id, text_tvrzeni, tvrditel, stav
FROM "07_Tvrzeni"
WHERE !podpora_dukazy AND !vyvraceni_dukazy
SORT datum_tvrzeni DESC
```

## Tvrzení podle osob

```dataview
TABLE id, text_tvrzeni, stav
FROM "07_Tvrzeni"
WHERE typ = "tvrzeni"
GROUP BY osoby
```
