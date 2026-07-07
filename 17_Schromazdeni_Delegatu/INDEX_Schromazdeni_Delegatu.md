---
id: SD-INDEX
typ: system
nazev: Přehled shromáždění delegátů TJ Krupka
datum: 2026-06-26
vytvoreno: 2026-06-26
upraveno: 2026-07-06
tagy:
  - schromazdeni-delegatu
  - prehled
  - index
---

# Přehled shromáždění delegátů TJ Krupka

> [!INFO] Struktura
> Tato složka obsahuje všechny události týkající se shromáždění delegátů (SD) TJ Krupka z.s.
> Každé SD má vlastní záznam UDA a je propojeno s klíčovou událostí [[KUDA-2026-006_Schromazdeni_delegatu]].

---

## Seznam shromáždění delegátů

| Datum | ID | Název | Stav | Klíčová událost |
|------:|----|-------|------|-----------------|
| 24.8.2021 | [[UDA-2026-002_Shromazdeni_delegatu_zvoleni_MB_24-8-2021\|UDA-2026-002]] | Zvolení M. Brožka předsedou | dokázáno | [[KUDA-2026-006_Schromazdeni_delegatu\|KUDA-2026-006]] |
| 19.10.2023 | [[UDA-2026-010_Nelegalni_shromazdeni_Vanis_19-10-2023\|UDA-2026-010]] | Neoprávněné SD svolané Vanišem | dokázáno | [[KUDA-2026-006_Schromazdeni_delegatu\|KUDA-2026-006]] |
| 7.12.2023 | [[UDA-2026-020_rousek_-_navrh_na_zruseni_shromazdeni_delegatu_2023-12-07\|UDA-2026-020]] | Rousek — návrh na zrušení SD | neověřeno | [[KUDA-2026-006_Schromazdeni_delegatu\|KUDA-2026-006]] |
| 14.1.2024 | [[UDA-2026-027_kooo_-_1_email_rouskovi_-_oznameni_a_oduvodneni_ne_2024-01-14\|UDA-2026-027]] | Oznámení Rouskovi o nedostatcích žádosti | neověřeno | [[KUDA-2026-006_Schromazdeni_delegatu\|KUDA-2026-006]] |
| 25.1.2024 | [[UDA-2026-005_SD_nove_stanovy_TO_25-1-2024\|UDA-2026-005]] | Nové stanovy + trestní oznámení | dokázáno | [[KUDA-2026-006_Schromazdeni_delegatu\|KUDA-2026-006]] |
| 25.1.2025 | [[UDA-2026-043_Mimořádné_SD_TJK_25-1-2025\|UDA-2026-043]] | SD 25.1.2025 | neověřeno | [[KUDA-2026-006_Schromazdeni_delegatu\|KUDA-2026-006]] |
| 16.4.2025 | [[UDA-2026-040_Mimořádné_SD_TJK_16-4-2025\|UDA-2026-040]] | Mimořádné SD 16.4.2025 | neověřeno | [[KUDA-2026-006_Schromazdeni_delegatu\|KUDA-2026-006]] |
| 29.6.2025 | [[UDA-2026-041_Mimořádné_SD_TJK_29-6-2025\|UDA-2026-041]] | Mimořádné SD 29.6.2025 | neověřeno | [[KUDA-2026-006_Schromazdeni_delegatu\|KUDA-2026-006]] |
| 26.4.2026 | [[UDA-2026-042_VYSÍLAČ_SD_TJK_26-4-2026\|UDA-2026-042]] | VYSÍLAČ — SD 26.4.2026 | neověřeno | [[KUDA-2026-006_Schromazdeni_delegatu\|KUDA-2026-006]] |

---

## Klíčová událost

- [[KUDA-2026-006_Schromazdeni_delegatu]] — souhrnná analýza všech SD

---

## Automatický přehled

```dataview
TABLE nazev AS "Název", datum AS "Datum", stav_vysetreni AS "Stav", klicova_udalost AS "KUDA"
FROM "17_Schromazdeni_Delegatu"
WHERE typ = "udalost"
SORT datum ASC
```

---

## Důkazy k dispozici

```dataview
TABLE datum, popis, stav_dukazu
FROM "04_Dukazy"
WHERE contains(udalosti.file.folder, "17_Schromazdeni_Delegatu") OR contains(udalosti, "UDA-2026-002") OR contains(udalosti, "UDA-2026-005") OR contains(udalosti, "UDA-2026-010") OR contains(udalosti, "UDA-2026-020") OR contains(udalosti, "UDA-2026-027") OR contains(udalosti, "UDA-2026-040") OR contains(udalosti, "UDA-2026-041") OR contains(udalosti, "UDA-2026-042") OR contains(udalosti, "UDA-2026-043")
SORT datum ASC
```

---

## Související přehledy

| Sekce | Odkaz |
|-------|-------|
| Klíčové události | [[../11_Klicove_Udalosti/INDEX_Klicove_Udalosti]] |
| Události | [[../03_Udalosti/\|Složka Události]] |
| Důkazy | [[../04_Dukazy/\|Složka Důkazy]] |
| Dashboard | [[../14_Dashboard/Hlavni_Dashboard\|Hlavní Dashboard]] |
| Infografika vazeb | [[../09_Vystupy/VYS-2026-002_Infografika_vazeb\|VYS-2026-002]] — vizuální mapa |
| Jednání s městem | [[ANL-2026-005_Prehled_jednani_Mesto_Krupka]] — role města v SD |

---

> [!CAUTION] Upozornění
> Záznamy pro roky 2025–2026 byly vytvořeny na základě dostupných dokumentů v Google Drive a vyžadují doplnění detailů o průběhu a usneseních.

## Tagy

#schromazdeni-delegatu #prehled #index
