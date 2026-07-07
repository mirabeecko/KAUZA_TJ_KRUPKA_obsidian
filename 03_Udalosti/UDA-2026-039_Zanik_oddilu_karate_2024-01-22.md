---
id: UDA-2026-039
typ: udalost
nazev: Zánik oddílu karate
datum: 2024-01-22
datum_do: 
cas: 
misto: 
kraj: 
popis: >
  Zánik oddílu karate v TJ Krupka. Dne 15.12.2023 byl předsedovi oddílu Martinu Kulíkovi zaslán výzva
  ke zjednání nápravy pro neuhrazené členské příspěvky. Dne 22.1.2024 bylo vydáno oznámení o zániku oddílu karate.
osoby:
  - "[[OSO-2026-001_Miroslav_Brozek]]"
  - "[[OSO-2026-005_Martin_Kulik]]"
organizace:
  - "[[ORG-2026-001_TJ_Krupka]]"
dokumenty:
dukazy:
  - "[[DUK-2023-011_Karate_vyzva_ke_zjednani_napravy_Kulik]]"
  - "[[DUK-2024-018_Oznameni_o_zaniku_karate_22-1-2024]]"
stav_vysetreni: overeno
stav_vysledku: planovano
vysledek: neurceno
relevance: stredni
duvernost: interni
vytvoreno: 2026-06-26
upraveno: 2026-06-26
tagy:
  - udalost
  - karate
  - zanik
  - oddil
  - kulik
---

# Zánik oddílu karate

## Základní identifikace

| Pole | Hodnota |
|------|---------|
| **ID** | UDA-2026-039 |
| **Datum** | 22.1.2024 |
| **Stav vyšetření** | ověřeno |
| **Stav výsledku** | plánováno |
| **Výsledek** | neurčeno |
| **Relevance** | střední |

## Popis události

> [!NOTE] Co se stalo
> Oddíl karate v TJ Krupka zanikl. Předcházela tomu výzva ke zjednání nápravy z 15.12.2023,
> která byla adresována předsedovi oddílu Martinu Kulíkovi. Výzva upozornila na neuhrazené
> členské příspěvky a hrozila vyloučením. Dne 22.1.2024 bylo vydáno oznámení o zániku oddílu karate.

## Chronologie

| Čas | Popis | Zdroj |
|-----|-------|-------|
| 15.12.2023 | Výzva ke zjednání nápravy pro Martina Kulíka | [[DUK-2023-011]] |
| 22.1.2024 | Oznámení o zániku oddílu karate | [[DUK-2024-018]] |

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

## Analytická hodnocení

> [!WARNING] Upozornění
> Obsah této sekce jsou analytické hypotézy — **ne fakta ani závěry**.

## Otevřené otázky

- [ ] Jaký byl přesný právní důvod zániku oddílu?
- [ ] Bylo oznámení o zániku řádně doručeno Martinu Kulíkovi?
- [ ] Jaké mají zánik oddílu dopady na majetek a členskou základnu?

## Zdroje a reference

- [[DUK-2023-011_Karate_vyzva_ke_zjednani_napravy_Kulik]]
- [[DUK-2024-018_Oznameni_o_zaniku_karate_22-1-2024]]
- [[OSO-2026-005_Martin_Kulik]]

## Související záznamy

- [[DUK-2023-011_Karate_vyzva_ke_zjednani_napravy_Kulik]]
- [[DUK-2024-018_Oznameni_o_zaniku_karate_22-1-2024]]
- [[ORG-2026-001_TJ_Krupka]]
- [[OSO-2026-005_Martin_Kulik]]
