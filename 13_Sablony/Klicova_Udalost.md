---
id: KUDA-RRRR-NNN
typ: klicova-udalost
nazev: 
datum: 
datum_do: 
cas: 
misto: 
kraj: 
popis: >
  
osoby: []
organizace: []
dokumenty: []
dukazy: []
podrizene_udalosti: []
stav_vysetreni: neovereno
stav_vysledku: planovano
vysledek: neurceno
relevance: klicova
duvernost: interni
vytvoreno: 2026-06-26
upraveno: 2026-06-26
tagy:
  - udalost
  - klicova-udalost
---

# Název klíčové události

## Základní identifikace

| Pole | Hodnota |
|------|---------|
| **ID** | KUDA-RRRR-NNN |
| **Období** | |
| **Místo** | |
| **Stav vyšetření** | neověřeno |
| **Stav výsledku** | plánováno |
| **Výsledek** | neurčeno |
| **Relevance** | klíčová |

## Shrnutí klíčové události

> [!CAUTION] Podstata problému
> Stručný, ale detailní popis celkového problému. Co se stalo, kdo to udělal, proč je to právně / organizačně významné.
> Uveďte konkrétní data, subjekty a důsledky.

## Právní / organizační kontext

| Zákon / předpis | Ustanovení | Jak bylo porušeno |
|---|---|---|
| [[ZAK-RRRR-NNN]] | § ... | |

## Chronologie

| Datum | Událost | Zdroj |
|------:|---------|-------|
| | | |

## Kdo je odpovědný

| Osoba / Subjekt | Role | Právní odpovědnost |
|---|---|---|
| | | |

## Dopad

- Jaký byl dopad na TJ Krupka?
- Jaký byl dopad na členy / děti / sportovní činnost?
- Jaký byl finanční / majetkový / procesní dopad?

## Postoj policie / soudu / úřadů

> [!WARNING] Postoj orgánů
> Jak se k události postavily státní orgány? Co bylo opomenuto?

## Podřízené události

- [[UDA-RRRR-NNN_Nazev_podrizene_udalosti]]

## Zúčastněné osoby

```dataview
TABLE id, cele_jmeno, role, organizace
FROM "01_Osoby"
WHERE contains(file.outlinks, this.file.link)
```

## Zúčastněné organizace

```dataview
TABLE id, nazev, ico
FROM "02_Organizace"
WHERE contains(file.outlinks, this.file.link)
```

## Dokumenty

```dataview
TABLE datum, typ, nazev, autor
FROM "05_Dokumenty"
WHERE contains(udalosti, this.file.name)
SORT datum ASC
```

## Důkazy

```dataview
TABLE datum, typ, zdroj, stav_dukazu
FROM "04_Dukazy"
WHERE contains(udalosti, this.file.name)
SORT datum ASC
```

## Tvrzení

```dataview
TABLE text_tvrzeni, stav, osoby
FROM "07_Tvrzeni"
WHERE contains(udalosti, this.file.name)
```

## Otevřené otázky

- [ ] 

## Zdroje a reference

- 

## Související záznamy

- 
