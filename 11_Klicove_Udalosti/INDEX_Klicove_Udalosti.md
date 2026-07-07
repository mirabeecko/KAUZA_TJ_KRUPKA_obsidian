---
id: KUDA-INDEX
typ: system
nazev: Přehled klíčových událostí kauzy TJK
datum: 2026-06-26
vytvoreno: 2026-06-26
upraveno: 2026-07-06
tagy:
  - klicova-udalost
  - prehled
  - index
---

# Přehled klíčových událostí kauzy TJK

> [!INFO] Co jsou klíčové události
> Klíčové události (KUDA) shrnují skupiny navzájem souvisejících dílčích událostí, které tvoří jednotlivá jádra kauzy TJ Krupka.
> Každá klíčová událost má vlastní ID `KUDA-RRRR-NNN`, vlastní složku `11_Klicove_Udalosti/` a slouží jako vzorová struktura pro analýzu.

---

## Seznam klíčových událostí

| ID | Název | Období | Stav vyšetření | Podřízených událostí |
|----|-------|--------|---------------|----------------------|
| KUDA-2026-001 | [[KUDA-2026-001_CAST_ignorace_a_porusovani_pravidel\|ČÁST — ignorace a porušování pravidel]] | 2021–2024 | částečně ověřeno | — |
| KUDA-2026-002 | [[KUDA-2026-002_Vylouceni_clenu_a_zanik_clenstvi\|Vyloučení členů a zánik členství]] | 2023–2024 | ověřeno | — |
| KUDA-2026-003 | [[KUDA-2026-003_Trestni_oznameni_a_policni_rizeni\|Trestní oznámení a policejní řízení]] | 2024–2025 | částečně ověřeno | — |
| KUDA-2026-004 | [[KUDA-2026-004_Spor_o_predsednictvi_a_obchodni_rejstrik\|Spor o předsednictví a obchodní rejstřík]] | 2021–2025 | ověřeno | — |
| KUDA-2026-005 | [[KUDA-2026-005_Znemožnění_přístupu_do_pinčesárny\|Znemožnění přístupu do pinčesárny]] | 6.12.2023 – 19.1.2024 | částečně ověřeno | 9 |
| KUDA-2026-006 | [[KUDA-2026-006_Schromazdeni_delegatu\|Shromáždění delegátů TJ Krupka]] | 24.8.2021 – 26.4.2026 | částečně ověřeno | 9 |

---

## Automatický přehled

```dataview
TABLE nazev AS "Název", datum AS "Od", datum_do AS "Do", stav_vysetreni AS "Stav vyšetření", length(podrizene_udalosti) AS "Podřízené události"
FROM "11_Klicove_Udalosti"
WHERE typ = "klicova-udalost"
SORT id ASC
```

---

## Šablona

Pro vytvoření nové klíčové události použijte šablonu: [[../13_Sablony/Klicova_Udalost\|Šablona klíčové události]]

---

## Související přehledy

| Sekce | Odkaz |
|-------|-------|
| Události | [[../03_Udalosti/\|Složka Události]] |
| Důkazy | [[../04_Dukazy/\|Složka Důkazy]] |
| Dashboard | [[../14_Dashboard/Hlavni_Dashboard\|Hlavní Dashboard]] |
| Přehled jednání s Lesy ČR | [[ANL-2026-004_Prehled_jednani_Lesy_CR]] |
| Přehled jednání s městem | [[ANL-2026-005_Prehled_jednani_Mesto_Krupka]] |
| Přehled bývalých členů | [[ANL-2026-006_Prehled_byvali_clenove]] |
| Sporné položky | [[09_Vystupy/SPORNE_POLOZKY_KE_SCHVALENI\|Sporné položky ke schválení]] |

---

## Související nové dokumenty (web)

Dokumenty vytvořené na základě analýzy webu tjk.manus.space:

- [[ANL-2026-004_Prehled_jednani_Lesy_CR]] — přehled jednání s Lesy ČR
- [[ANL-2026-005_Prehled_jednani_Mesto_Krupka]] — přehled jednání s městem
- [[ANL-2026-006_Prehled_byvali_clenove]] — přehled bývalých členů
- [[../09_Vystupy/VYS-2026-001_Prehled_kauzy_pro_web\|VYS-2026-001]] — přehled kauzy
- [[../09_Vystupy/VYS-2026-002_Infografika_vazeb\|VYS-2026-002]] — infografika vazeb
- [[../09_Vystupy/SPORNE_POLOZKY_KE_SCHVALENI\|Sporné položky ke schválení]] — sporné položky

---

> [!CAUTION] Upozornění
> Klíčové události jsou analytickým shrnutím. Konkrétní fakta musí být vždy ověřena proti originálním důkazům a právním dokumentům.

## Tagy

#klicova-udalost #prehled #index
