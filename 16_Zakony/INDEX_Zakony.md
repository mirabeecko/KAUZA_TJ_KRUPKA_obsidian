---
id: ZAK-INDEX
typ: system
nazev: Přehled zákonů v kauze TJK
tagy:
  - zakon
  - prehled
  - index
---

# Přehled zákonů použitých v kauze TJK

> [!INFO] Struktura zákonů
> Každý zákon je uložen jako samostatný soubor v této složce. Paragrafy použité v kauze TJK jsou vyznačeny jako nadpisy s odkazem na konkrétní dokumenty, kde se vyskytují.

---

## Seznam zákonů

| ID | Název zákona | Číslo | Odkaz | Použité § v kauze |
|----|-------------|-------|-------|------------------|
| ZAK-2026-001 | **Trestní zákoník** | 40/2009 Sb. | [[ZAK-2026-001_Trestni_zakonik_40_2009]] | § 24, 175, 184, 206, 207, 208, 209, 220, 228, 254, 329 |
| ZAK-2026-002 | **Trestní řád** | 141/1961 Sb. | [[ZAK-2026-002_Trestni_rad_141_1961]] | § 2, 78, 89, 157, 158, 164, 174 |
| ZAK-2026-003 | **Občanský zákoník** | 89/2012 Sb. | [[ZAK-2026-003_Obcansky_zakonik_89_2012]] | § 3, 6, 8, 159, 1970, 2205, 2209, 238, 239, 259, 2910, 2915, 2991 |
| ZAK-2026-004 | **Zákon o veřejných rejstřících** | 304/2013 Sb. | [[ZAK-2026-004_Zakon_o_verejnych_rejstrikch_304_2013]] | § 11 |
| ZAK-2026-005 | **Občanský soudní řád** | 99/1963 Sb. | [[ZAK-2026-005_Obcansky_soudni_rad_99_1963]] | § 57, 86, 142, 202 |
| ZAK-2026-006 | **Zákon o obcích** | 128/2000 Sb. | [[ZAK-2026-006_Zakon_o_obcich_128_2000]] | § 38 |
| ZAK-2026-007 | **Zákon o obětech trestných činů** | 45/2013 Sb. | [[ZAK-2026-007_Zakon_o_obetech_trestnych_cinu_45_2013]] | § 16 |
| ZAK-2026-008 | **Trestní odpovědnost právnických osob** | 418/2011 Sb. | [[ZAK-2026-008_Trestni_odpovednost_pravnickych_osob_418_2011]] | § 8 |
| ZAK-2026-009 | **Zákon o soudních poplatcích** | 549/1991 Sb. | [[ZAK-2026-009_Zakon_o_soudnich_poplatcich_549_1991]] | § 2 |
| ZAK-2026-010 | **Zákon o zadávání veřejných zakázek** | 134/2016 Sb. | [[ZAK-2026-010_Zakon_o_zadavani_verejnych_zakazek_134_2016]] | § 17 |
| ZAK-2026-011 | **Zákon o policii** | 273/2008 Sb. | [[ZAK-2026-011_Zakon_o_policicnich_273_2008]] | Připraveno pro budoucí použití |

---

## Jak odkazy fungují

V libovolném dokumentu kauze TJK se nyní můžete setkat s odkazy jako:

- `[[ZAK-2026-001_Trestni_zakonik_40_2009#§ 208|§ 208 TZ]]`
- `[[ZAK-2026-003_Obcansky_zakonik_89_2012#§ 2991|§ 2991 OZ]]`

Kliknutím na odkaz se přesunete přímo na daný paragraf v příslušném zákoníku.

## Automatický přehled použití

```dataview
TABLE nazev AS "Název zákona", count(file.inlinks) AS "Počet odkazů z kauzy"
FROM "16_Zakony"
WHERE typ = "zakon"
SORT count(file.inlinks) DESC
```

## Externí zdroje pro ověření znění

- [zakonyprolidi.cz](https://www.zakonyprolidi.cz/) — aktuální znění všech zákonů
- [e-sbirka.cz](https://www.e-sbirka.cz/) — oficiální Sbírka zákonů ČR

---

> [!CAUTION] Upozornění
> Znění paragrafů v těchto souborech je uvedeno v podobě platné k datu vytvoření (červen 2026). Pro aktuální znění vždy použijte oficiální zdroje. U paragrafů označených `[!WARNING] Znění ke kontrole` doporučujeme ověřit aktuální znění před právním použitím.

## Tagy

#zakon #pravni_predpis #prehled #index
