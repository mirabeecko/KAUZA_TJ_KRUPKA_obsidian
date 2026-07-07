---
id: UDA-2026-028
typ: udalost
nazev: Stížnosti ČAST na převod soutěží, přestupy a výchovné
datum: 2024-01-15
datum_do: 
cas: 
misto: 
kraj: 
popis: >
  Podání stížností České asociaci stolního tenisu (ČAST) týkajících se neoprávněného převodu soutěží,
  neplatných přestupů hráčů stolního tenisu a neuhrazeného výchovného TJ Krupka.
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
  - stížnost
  - stolní-tenis
  - přestup
  - převod-soutěží
  - výchovné
---

# Stížnosti ČAST na převod soutěží, přestupy a výchovné

## Základní identifikace

| Pole | Hodnota |
|------|---------|
| **ID** | UDA-2026-028 |
| **Datum** | 15.1.2024 |
| **Stav vyšetření** | částečně ověřeno |
| **Stav výsledku** | plánováno |
| **Výsledek** | neurčeno |
| **Relevance** | vysoká |

## Popis události

> [!NOTE] Co se stalo
> TJ Krupka podala České asociaci stolního tenisu (ČAST) stížnosti týkající se:
> 1. Neoprávněného převodu/přechodu soutěží stolního tenisu od TJ k jinému subjektu.
> 2. Neplatných přestupů hráčů stolního tenisu bez souhlasu TJ.
> 3. Neuhrazeného výchovného za odchozí hráče.
>
> Tato podání jsou součástí širšího problému nečinnosti ČAST řešeného v rámci
> [[KUDA-2026-001_CAST_ignorace_a_porusovani_pravidel|klíčové události ČAST]].

## Chronologie

| Čas | Popis | Zdroj |
|-----|-------|-------|
| 15.1.2024 | Podání stížností ČAST | DUK-2025-018, DUK-2025-034 až 036 |

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

- [ ] Jakým způsobem byly stížnosti ČAST doručeny?
- [ ] Existuje doručenka nebo potvrzení o přijetí?
- [ ] Jaké lhůty pro vyřízení stanoví disciplinární řád ČAST?

## Zdroje a reference

- [[KUDA-2026-001_CAST_ignorace_a_porusovani_pravidel]]
- [[DUK-2025-018_Stížnost_na_neoprávněný_převod_soutěží_TJ_Krupka_(GDoc)]]
- [[DUK-2025-034_Stížnost_na_neoprávněný_převodpřechod_soutěží_TJ_Krupka]]
- [[DUK-2025-035_Stížnost_na_neplatné_přestupy_hráčů_ST]]
- [[DUK-2025-036_Stížnost_na_neuhrazení_výchovného]]
- [[ORG-2026-004_CAST]]

## Související záznamy

- [[KUDA-2026-001_CAST_ignorace_a_porusovani_pravidel]]
- [[DUK-2025-018_Stížnost_na_neoprávněný_převod_soutěží_TJ_Krupka_(GDoc)]]
- [[DUK-2025-034_Stížnost_na_neoprávněný_převodpřechod_soutěží_TJ_Krupka]]
- [[DUK-2025-035_Stížnost_na_neplatné_přestupy_hráčů_ST]]
- [[DUK-2025-036_Stížnost_na_neuhrazení_výchovného]]
- [[ORG-2026-001_TJ_Krupka]]
- [[ORG-2026-004_CAST]]
