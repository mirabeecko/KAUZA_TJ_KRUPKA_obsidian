---
id: KUDA-2026-001
typ: klicova-udalost
nazev: ČAST — ignorance a porušování vlastních pravidel
datum: 2024-01-15
datum_do: 2025-12-24
cas: 
misto: 
kraj: 
popis: >
  Český asociace stolního tenisu (ČAST) a její krajské/regionální organizace (KSSTÚK, RSST Teplice)
  systematicky ignorovaly podané stížnosti TJ Krupka týkající se neoprávněného převodu soutěží,
  neplatných přestupů hráčů a neuhrazeného výchovného. Navzdory vlastním disciplinárním řádům
  a povinnosti rozhodovat o podáních nebylo ze strany ČAST učiněno žádné účinné opatření.
osoby:
  - "[[OSO-2026-001_Miroslav_Brozek]]"
organizace:
  - "[[ORG-2026-001_TJ_Krupka]]"
  - "[[ORG-2026-004_CAST]]"
dokumenty:
dukazy:
  - "[[DUK-2025-018_Stížnost_na_neoprávněný_převod_soutěží_TJ_Krupka_(GDoc)]]"
  - "[[DUK-2025-034_Stížnost_na_neoprávněný_převodpřechod_soutěží_TJ_Krupka]]"
  - "[[DUK-2025-035_Stížnost_na_neplatné_přestupy_hráčů_ST]]"
  - "[[DUK-2025-036_Stížnost_na_neuhrazení_výchovného]]"
  - "[[DUK-2025-037_Oznámení_zaslaná_ČAST_+_KSSTÚK_+_RSST_Teplice]]"
podrizene_udalosti:
  - "[[UDA-2026-028_Stiznosti_CAST_na_prevod_soutezi_prestupy_a_vychovne_2024-01-15]]"
  - "[[UDA-2026-033_Oznameni_CAST_KSSTUK_RSST_o_poruseni_pravidel_2024-01-22]]"
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
  - ČAST
  - stížnost
  - stolní-tenis
  - přestup
  - převod-soutěží
  - výchovné
---

# ČAST — ignorance a porušování vlastních pravidel

## Základní identifikace

| Pole | Hodnota |
|------|---------|
| **ID** | KUDA-2026-001 |
| **Období** | 15.1.2024 – 24.12.2025 |
| **Stav vyšetření** | částečně ověřeno |
| **Stav výsledku** | plánováno |
| **Výsledek** | neurčeno |
| **Relevance** | vysoká |

## Shrnutí klíčové události

> [!NOTE] Podstata problému
> TJ Krupka opakovaně podávala Českou asociaci stolního tenisu (ČAST) a jejím krajským organizacím
> stížnosti na neoprávněný převod soutěží, neplatné přestupy hráčů a neuhrazené výchovné.
> ČAST tyto podněty nevyřešila v souladu s vlastními řády, čímž došlo k porušení její povinnosti
> hájit zájmy členských oddílů a dodržovat vlastní disciplinární předpisy.

## Chronologie

| Čas        | Popis                                                        | Zdroj                                                                            |
| ---------- | ------------------------------------------------------------ | -------------------------------------------------------------------------------- |
| 15.1.2024  | Příprava a podání prvních stížností ČAST                     | [[UDA-2026-028_Stiznosti_CAST_na_prevod_soutezi_prestupy_a_vychovne_2024-01-15]] |
| 22.1.2024  | Hromadné oznámení ČAST, KSSTÚK a RSST Teplice                | [[UDA-2026-033_Oznameni_CAST_KSSTUK_RSST_o_poruseni_pravidel_2024-01-22]]        |
| 24.12.2025 | Opakované stížnosti a oznámení zůstaly bez účinného vyřízení | DUK-2025-034 až 037                                                              |

## Podřízené události

- [[UDA-2026-028_Stiznosti_CAST_na_prevod_soutezi_prestupy_a_vychovne_2024-01-15]]
- [[UDA-2026-033_Oznameni_CAST_KSSTUK_RSST_o_poruseni_pravidel_2024-01-22]]

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

- [ ] Jaké konkrétní řídící orgány ČAST byly o stížnostech informovány?
- [ ] Existuje písemné vyjádření ČAST k jednotlivým podáním?
- [ ] Bylo zahájeno disciplinární řízení nebo byla podání formálně odmítnuta?
- [ ] Jaké právní důsledky má nečinnost ČAST pro TJ Krupka?

## Zdroje a reference

- [[ORG-2026-004_CAST]]
- [[DUK-2025-018_Stížnost_na_neoprávněný_převod_soutěží_TJ_Krupka_(GDoc)]]
- [[DUK-2025-034_Stížnost_na_neoprávněný_převodpřechod_soutěží_TJ_Krupka]]
- [[DUK-2025-035_Stížnost_na_neplatné_přestupy_hráčů_ST]]
- [[DUK-2025-036_Stížnost_na_neuhrazení_výchovného]]
- [[DUK-2025-037_Oznámení_zaslaná_ČAST_+_KSSTÚK_+_RSST_Teplice]]

## Související záznamy

- [[UDA-2026-028_Stiznosti_CAST_na_prevod_soutezi_prestupy_a_vychovne_2024-01-15]]
- [[UDA-2026-033_Oznameni_CAST_KSSTUK_RSST_o_poruseni_pravidel_2024-01-22]]
- [[ORG-2026-004_CAST]]
- [[ORG-2026-001_TJ_Krupka]]
