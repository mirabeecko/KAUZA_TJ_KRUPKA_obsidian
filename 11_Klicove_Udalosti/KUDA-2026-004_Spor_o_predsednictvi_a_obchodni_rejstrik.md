---
id: KUDA-2026-004
typ: klicova-udalost
nazev: Spor o předsednictví a zápis v obchodním rejstříku
datum: 2021-08-24
datum_do: 2026-02-11
cas: 
misto: 
kraj: 
popis: >
  Spor o to, kdo je oprávněným předsedou TJ Krupka z.s. a kdo je řádně zapsán v obchodním rejstříku.
  Zahrnuje volbu předsedy, neoprávněná shromáždění, návrhy na výmaz a soudní rozhodnutí.
osoby:
  - "[[OSO-2026-001_Miroslav_Brozek]]"
  - "[[OSO-2026-004_Gustav_Vlach]]"
  - "[[OSO-2026-010_JUDr_Rousek]]"
organizace:
  - "[[ORG-2026-001_TJ_Krupka]]"
  - "[[ORG-2026-002_Mesto_Krupka]]"
dokumenty:
dukazy:
  - "[[DUK-2021-004_Zápis_z_valné_hromady_—_zvolení_Brožka_předsedou]]"
  - "[[DUK-2025-020_Usnesení_KS_—_nicotné_vyloučení]]"
  - "[[DUK-2025-021_Zápis_z_mimořádného_shromáždění_delegátů]]"
  - "[[DUK-2025-022_Zápis_z_mimořádného_shromáždění_delegátů]]"
  - "[[DUK-2025-024_Odvolání_—_výmaz_předsedy_spolku_(OR)]]"
  - "[[DUK-2025-025_Usnesení_KS_Ústí_—_odmítnutí_návrhu_na_zápis_změn_v_OR]]"
  - "[[DUK-2026-012_Kompletní_tabulka_OR_—_všechna_podání_L_318]]"
  - "[[DUK-2026-013_Detailní_analýza_osob_financí_a_práva]]"
  - "[[DUK-2026-015_⚠️_Aktuální_stav_OR_TJ_Krupka]]"
podrizene_udalosti:
  - "[[UDA-2026-002_Shromazdeni_delegatu_zvoleni_MB_24-8-2021]]"
  - "[[UDA-2026-009_Vitezstvi_Zdrazil_OR_26-9-2025]]"
  - "[[UDA-2026-010_Nelegalni_shromazdeni_Vanis_19-10-2023]]"
  - "[[UDA-2026-020_rousek_-_navrh_na_zruseni_shromazdeni_delegatu_2023-12-07]]"
  - "[[UDA-2026-037_schuzka_hygiena_obdrzeni_zaloby_na_tj_od_krajskeho_2025-02-11]]"
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
  - predseda
  - obchodni-rejstrik
  - OR
  - Vlach
  - Brozek
---

# Spor o předsednictví a zápis v obchodním rejstříku

## Základní identifikace

| Pole | Hodnota |
|------|---------|
| **ID** | KUDA-2026-004 |
| **Období** | 24.8.2021 – 11.2.2025 |
| **Stav vyšetření** | částečně ověřeno |
| **Stav výsledku** | plánováno |
| **Výsledek** | neurčeno |
| **Relevance** | vysoká |

## Shrnutí klíčové události

> [!NOTE] Podstata problému
> Miroslav Brožek byl zvolen předsedou TJ Krupka na shromáždění delegátů 24.8.2021. Později se objevily pokusy
> o jeho výmaz z obchodního rejstříku a o zpochybnění platnosti jeho předsednictví. Soudy zatím Brožkovu pozici
> jako předsedy podporují.

## Chronologie

| Čas | Popis | Zdroj |
|-----|-------|-------|
| 24.8.2021 | Zvolení Brožka předsedou | [[UDA-2026-002_Shromazdeni_delegatu_zvoleni_MB_24-8-2021]] |
| 19.10.2023 | Neoprávněné shromáždění svolané Vanišem | [[UDA-2026-010_Nelegalni_shromazdeni_Vanis_19-10-2023]] |
| 7.12.2023 | Návrh na zrušení shromáždění delegátů | [[UDA-2026-020_rousek_-_navrh_na_zruseni_shromazdeni_delegatu_2023-12-07]] |
| 26.9.2025 | Zdražil odmítl návrh Vlacha na výmaz Brožka z OR | [[UDA-2026-009_Vitezstvi_Zdrazil_OR_26-9-2025]] |
| 11.2.2025 | Schůzka hygiena, obdržení žaloby | [[UDA-2026-037_schuzka_hygiena_obdrzeni_zaloby_na_tj_od_krajskeho_2025-02-11]] |

## Podřízené události

- [[UDA-2026-002_Shromazdeni_delegatu_zvoleni_MB_24-8-2021]]
- [[UDA-2026-009_Vitezstvi_Zdrazil_OR_26-9-2025]]
- [[UDA-2026-010_Nelegalni_shromazdeni_Vanis_19-10-2023]]
- [[UDA-2026-020_rousek_-_navrh_na_zruseni_shromazdeni_delegatu_2023-12-07]]
- [[UDA-2026-037_schuzka_hygiena_obdrzeni_zaloby_na_tj_od_krajskeho_2025-02-11]]

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

- [ ] Jaké jsou všechny podání v rejstříkovém řízení L 318?
- [ ] Kdo zastupuje TJ Krupka v aktuálních soudních sporech?
- [ ] Jaký je vztah mezi sporem o předsedu a trestním oznámením?

## Zdroje a reference

- [[DUK-2021-004_Zápis_z_valné_hromady_—_zvolení_Brožka_předsedou]]
- [[DUK-2025-025_Usnesení_KS_Ústí_—_odmítnutí_návrhu_na_zápis_změn_v_OR]]
- [[DUK-2026-015_⚠️_Aktuální_stav_OR_TJ_Krupka]]

## Související záznamy

- [[UDA-2026-002_Shromazdeni_delegatu_zvoleni_MB_24-8-2021]]
- [[UDA-2026-009_Vitezstvi_Zdrazil_OR_26-9-2025]]
- [[UDA-2026-010_Nelegalni_shromazdeni_Vanis_19-10-2023]]
- [[ORG-2026-001_TJ_Krupka]]
- [[ORG-2026-002_Mesto_Krupka]]
