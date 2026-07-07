---
id: KUDA-2026-003
typ: klicova-udalost
nazev: Trestní oznámení a policejní řízení TJK
datum: 2022-07-28
datum_do: 2024-05-31
cas: 
misto: 
kraj: 
popis: >
  Trestní oznámení podaná TJ Krupka a policejní řízení vedená proti bývalým členům a spolupracovníkům.
  Zahrnuje jak původní šetření kriminální policií, tak pozdější trestní oznámení z ledna 2024 a jeho odložení.
osoby:
  - "[[OSO-2026-001_Miroslav_Brozek]]"
  - "[[OSO-2026-007_Blazicek_kriminalista]]"
organizace:
  - "[[ORG-2026-001_TJ_Krupka]]"
dokumenty:
dukazy:
  - "[[DUK-2024-002_Trestní_oznámení_TJ_Krupka]]"
  - "[[DUK-2024-016_Vyrozumění_TO_—_por._Blažíček_(240531)]]"
  - "[[DUK-2026-001_Policejni_vyrozumeni_Blazicek_31-5-2024]]"
podrizene_udalosti:
  - "[[UDA-2026-006_Podani_TO_25-1-2024]]"
  - "[[UDA-2026-007_Odlozeni_TO_policie_31-5-2024]]"
  - "[[UDA-2026-012_zahajeni_vysetrovani_krimi_-_roucek_2022-07-28]]"
stav_vysetreni: overeno_castecne
stav_vysledku: planovano
vysledek: neurceno
relevance: vysoka
duvernost: interni
vytvoreno: 2026-06-26
upraveno: 2026-06-26
tagy:
  - udalost
  - klicova-udalost
  - trestni-oznameni
  - policie
  - kriminalni-rizeni
---

# Trestní oznámení a policejní řízení TJK

## Základní identifikace

| Pole | Hodnota |
|------|---------|
| **ID** | KUDA-2026-003 |
| **Období** | 28.7.2022 – 31.5.2024 |
| **Stav vyšetření** | částečně ověřeno |
| **Stav výsledku** | plánováno |
| **Výsledek** | neurčeno |
| **Relevance** | vysoká |

## Shrnutí klíčové události

> [!NOTE] Podstata problému
> TJ Krupka podala trestní oznámení na bývalé členy a spolupracovníky pro podezření z hospodářské kriminality.
> Policie ČR řízení odložila s odůvodněním, že se nepodařilo prokázat trestný čin. Spolek tento postup kritizuje
> jako povrchní a neúplný.

## Chronologie

| Čas | Popis | Zdroj |
|-----|-------|-------|
| 28.7.2022 | Zahájení vyšetřování kriminální policií | [[UDA-2026-012_zahajeni_vysetrovani_krimi_-_roucek_2022-07-28]] |
| 25.1.2024 | Podání trestního oznámení na OSZ Teplice | [[UDA-2026-006_Podani_TO_25-1-2024]] |
| 31.5.2024 | Policie odložila trestní oznámení | [[UDA-2026-007_Odlozeni_TO_policie_31-5-2024]] |

## Podřízené události

- [[UDA-2026-006_Podani_TO_25-1-2024]]
- [[UDA-2026-007_Odlozeni_TO_policie_31-5-2024]]
- [[UDA-2026-012_zahajeni_vysetrovani_krimi_-_roucek_2022-07-28]]

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

- [ ] Jaké konkrétní skutky byly předmětem trestního oznámení?
- [ ] Proč policie oznámení odložila?
- [ ] Existuje možnost podat stížnost proti odložení?

## Zdroje a reference

- [[DUK-2024-002_Trestní_oznámení_TJ_Krupka]]
- [[DUK-2026-001_Policejni_vyrozumeni_Blazicek_31-5-2024]]
- [[OSO-2026-007_Blazicek_kriminalista]]

## Související záznamy

- [[UDA-2026-006_Podani_TO_25-1-2024]]
- [[UDA-2026-007_Odlozeni_TO_policie_31-5-2024]]
- [[UDA-2026-012_zahajeni_vysetrovani_krimi_-_roucek_2022-07-28]]
- [[ORG-2026-001_TJ_Krupka]]
