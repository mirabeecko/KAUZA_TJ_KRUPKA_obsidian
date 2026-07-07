---
id: UDA-2026-033
typ: udalost
nazev: Oznámení ČAST, KSSTÚK a RSST Teplice o porušení pravidel
datum: 2024-01-22
datum_do: 
cas: 
misto: 
kraj: 
popis: >
  Hromadné oznámení zaslané České asociaci stolního tenisu (ČAST), Krajskému svazu stolního tenisu Ústeckého kraje (KSSTÚK)
  a Regionálnímu svazu stolního tenisu Teplice (RSST Teplice) o porušení pravidel v oddíle stolního tenisu.
osoby:
  - "[[OSO-2026-001_Miroslav_Brozek]]"
organizace:
  - "[[ORG-2026-001_TJ_Krupka]]"
  - "[[ORG-2026-004_CAST]]"
dokumenty:
dukazy:
  - "[[DUK-2025-037_Oznámení_zaslaná_ČAST_+_KSSTÚK_+_RSST_Teplice]]"
klicova_udalost: "[[KUDA-2026-001_CAST_ignorace_a_porusovani_pravidel]]"
stav_vysetreni: overeno_castecne
stav_vysledku: planovano
vysledek: neurceno
relevance: vysoka
duvernost: interni
vytvoreno: 2026-06-25
upraveno: 2026-06-26
tagy:
  - udalost
  - ČAST
  - KSSTÚK
  - RSST
  - oznámení
  - stolní-tenis
  - porušení-pravidel
---

# Oznámení ČAST, KSSTÚK a RSST Teplice o porušení pravidel

## Základní identifikace

| Pole | Hodnota |
|------|---------|
| **ID** | UDA-2026-033 |
| **Datum** | 22.1.2024 |
| **Stav vyšetření** | částečně ověřeno |
| **Stav výsledku** | plánováno |
| **Výsledek** | neurčeno |
| **Relevance** | vysoká |

## Popis události

> [!NOTE] Co se stalo
> TJ Krupka zaslala hromadné oznámení České asociaci stolního tenisu (ČAST),
> Krajskému svazu stolního tenisu Ústeckého kraje (KSSTÚK) a Regionálnímu svazu
> stolního tenisu Teplice (RSST Teplice) o porušení pravidel v oddíle stolního tenisu.
> Toto oznámení je součástí širšího problému nečinnosti ČAST řešeného v rámci
> [[KUDA-2026-001_CAST_ignorace_a_porusovani_pravidel|klíčové události ČAST]].

## Chronologie

| Čas | Popis | Zdroj |
|-----|-------|-------|
| 22.1.2024 | Odeslání hromadného oznámení ČAST, KSSTÚK, RSST Teplice | DUK-2025-037 |

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

- [ ] Komu konkrétně bylo oznámení adresováno?
- [ ] Existuje doručenka nebo potvrzení o přijetí?
- [ ] Jakým způsobem bylo oznámení doručeno (datovka, e-mail, pošta)?

## Zdroje a reference

- [[KUDA-2026-001_CAST_ignorace_a_porusovani_pravidel]]
- [[DUK-2025-037_Oznámení_zaslaná_ČAST_+_KSSTÚK_+_RSST_Teplice]]
- [[ORG-2026-004_CAST]]

## Související záznamy

- [[KUDA-2026-001_CAST_ignorace_a_porusovani_pravidel]]
- [[UDA-2026-028_Stiznosti_CAST_na_prevod_soutezi_prestupy_a_vychovne_2024-01-15]]
- [[DUK-2025-037_Oznámení_zaslaná_ČAST_+_KSSTÚK_+_RSST_Teplice]]
- [[ORG-2026-001_TJ_Krupka]]
- [[ORG-2026-004_CAST]]
