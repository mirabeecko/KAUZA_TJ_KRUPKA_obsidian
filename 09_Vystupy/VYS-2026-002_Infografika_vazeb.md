---
id: VYS-2026-002
typ: vystup
nazev: Infografika vazeb — aktéři a vztahy v kauze TJ Krupka
datum: 2026-07-06
vytvoreno: 2026-07-06
upraveno: 2026-07-06
tagy:
  - NOVÉ
  - infografika
  - vazby
  - akteri
  - web
stav: k_recenzi
zdroj: "https://tjk.manus.space"
web_sekce: infografika
---

# Infografika vazeb — Aktéři a vztahy

> [!NOTE] Textová reprezentace infografiky
> Tento dokument zachycuje textovou podobu relační mapy z webové prezentace kauzy.
> Slouží jako podklad pro vizualizaci vazeb mezi klíčovými aktéry.

---

## 1. Hlavní mocenský trojúhelník

```
┌──────────────────────┐
│    MĚSTO KRUPKA      │
│   (ORG-2026-002)     │
│                      │
│  Starosta: Kuzma    │
│  Radní:    Bokoč    │
│  Zastup.:  Vítů     │
└────────┬─────────────┘
         │
         │ 100% vlastník
         ▼
┌──────────────────────┐      ┌──────────────────────┐
│ SPORT Krupka s.r.o.  │◄────►│     LESY ČR s.p.     │
│   (ORG-2026-003)     │      │                      │
│                      │      │  Údajná pohledávka   │
│  Jednatel: Vítů     │      │  cca 500 000 Kč      │
│  Vlastník: Kuzma    │      │  Směna pozemků       │
└────────┬─────────────┘      └──────────────────────┘
         │
         │ provozuje
         ▼
┌──────────────────────┐
│     PINČESÁRNA       │
│   (Lyžařský areál    │
│    Komáří vížka)     │
└──────────────────────┘
```

---

## 2. Klíčové osoby a jejich vztahy

### Jan Kuzma — [[OSO-2026-018_Jan_Kuzma_starosta]]
```
Starosta Krupky ──┐
                  ├── 100% vlastník SPORT Krupka s.r.o.
                  ├── Pověřen jednáním s TJK (UR-899) — nejednal
                  ├── Schvaluje dotace — TJK nedostává nic
                  └── Hlasuje o usneseních týkajících se vlastní firmy
```

### Jan Bokoč — [[OSO-2026-008_Jan_Bokoc]]
```
Radní města ──┐
              ├── Volební program: "Převzetí areálu Komáří vížka"  ← MOTIV
              ├── Pověřen jednáním s TJK (UR-899) — nejednal
              ├── Oznamuje splnění mandátu bez reálného jednání
              └── Navrhuje koupi dluhu → likvidaci TJK
```

### Adolf Vítů — [[OSO-2026-009_Adolf_Vitu]]
```
Zastupitel města ──┐
                   ├── Jednatel SPORT Krupka s.r.o.
                   ├── Hlasuje pro UR-314, 315, 316 (vlastní prospěch)
                   └── Střet zájmů (§ 83 zákona o obcích)
```

### Marek Vaniš — [[OSO-2026-002_Marek_Vanis]]
```
Bývalý člen TJK ──┐
                  ├── Svolal neoprávněné SD (19.10.2023)
                  ├── Pokusil se převést majetek TJK na město → § 209 TZ
                  ├── 2× vyloučen (2023 nicotné, 2026 nové)
                  ├── KST Krupka z.s. — převzal hráče a soutěže TJK
                  └── Právník: JUDr. Rousek
```

### Jaromír Pivoňka — [[OSO-2026-003_Jaromir_Pivonka]]
```
Bývalý člen TJK ──┐
                  ├── 2× vyloučen (spolu s Vanišem)
                  ├── Spolupracovník Vaniše v KST Krupka
                  ├── WhatsApp důkazy o záměrech
                  └── Právník: JUDr. Rousek
```

### Gustav Vlach — [[OSO-2026-004_Gustav_Vlach]]
```
Bývalý člen TJK ──┐
                  ├── Zánik členství 23.12.2023 (sporný)
                  ├── Návrh na opatrovníka — zamítnut
                  ├── Podání odmítnuto Zdražilem 26.9.2025 ✅
                  └── Právník: JUDr. Rousek
```

---

## 3. Vazby přes sportovní svazy

```
Vaniš + Pivoňka
       │
       ▼
┌──────────────────┐
│  KST Krupka z.s. │  ← založeno po vyloučení z TJK
│  (ORG-2026-007)  │
└────────┬─────────┘
         │ registrace
         ▼
┌──────────────────┐
│    KSSTÚK        │  ← prominul poplatky za přechod
│  (ORG-2026-006)  │     schválil převod soutěží
└────────┬─────────┘
         │ člen
         ▼
┌──────────────────┐
│     ČAST         │  ← ignoruje stížnosti TJK
│  (ORG-2026-004)  │
└──────────────────┘
```

---

## 4. Právní zastoupení

```
TJ Krupka z.s. ───────────► Mgr. Miroslav Kučera (advokát)
                               [[OSO-2026-015_Mgr_Kucera]]

Vaniš, Pivoňka, Vlach ────► JUDr. Jiří Rousek (advokát)
                               [[OSO-2026-010_JUDr_Rousek]]
```

---

## 5. Smyčky absurdity (přehled)

Viz podrobná analýza: [[❌ 90_shrnující_upřesňující_dokumenty_k_klíčovým_událostem/Smyčka Absurdity]].

| Osoba | Role A | Role B | Absurdní výsledek |
|-------|--------|--------|-------------------|
| **Bokoč** | Vyjednavač s TJK | Likvidátor TJK | Oznamuje splnění jednání, které nikdy neproběhlo |
| **Kuzma** | Starosta (dotace) | Vlastník SPORT Krupka | Odebírá dotace TJK ve prospěch vlastní firmy |
| **Vítů** | Zastupitel (hlasuje) | Jednatel SPORT Krupka | Hlasuje o převodu majetku do vlastní firmy |

> **Shrnutí:** Systém, kde tentýž člověk jedná za město, rozhoduje za město a zároveň profituje z rozhodnutí skrze svoji firmu.

---

## 6. Finanční toky

```
Město Krupka
  │
  ├── DOTACE → KST Krupka (310 000 Kč v 2025)
  ├── DOTACE → ostatní spolky
  ├── DOTACE → TJ Krupka: 0 Kč (od 2024)
  │
  ├── PLATBA → Lesy ČR (za směnu pozemků)
  ├── PLATBA → Lesy ČR (za postoupení pohledávky ~500 000 Kč)
  │
  └── PŘÍJEM → SPORT Krupka (z provozu areálu)
```

---

## 7. Související soubory

- [[VYS-2026-001_Prehled_kauzy_pro_web]] — Přehled kauzy
- [[❌ 90_shrnující_upřesňující_dokumenty_k_klíčovým_událostem/Smyčka Absurdity]] — Smyčky absurdity
- [[ANL-2026-004_Prehled_jednani_Lesy_CR]] — Přehled jednání s Lesy ČR
- [[ANL-2026-005_Prehled_jednani_Mesto_Krupka]] — Přehled jednání s městem
- [[ANL-2026-006_Prehled_byvali_clenove]] — Přehled bývalých členů
- [[ZIVE_SHRNUTI_KAUZY]] — Živé shrnutí
- [[DUK-2026-020_Volebni_program_Bokoce]] — Volební program Bokoče (MOTIV)
