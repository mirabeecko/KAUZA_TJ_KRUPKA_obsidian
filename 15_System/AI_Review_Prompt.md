---
typ: system
nazev: AI Review — kontrola vaultu a návrh aktualizací
tagy:
  - system
  - review
  - ai
---

# AI Review — Průvodce kontrolou vaultu

> [!IMPORTANT] Jak spustit review
> Zkopírujte prompt z **Sekce 1** a odešlete do Claude Code (nebo Claude Desktop s MCP).
> Claude navrhne změny. Pro každý přehled zvlášť potvrďte nebo odmítněte.

---

## SEKCE 1 — HLAVNÍ REVIEW PROMPT

```
Proveď review vaultu TJ Krupka na cestě:
/Users/mb/Documents/KAUZA_TJ_KRUPKA_obsidian/

KROK 1 — ZJISTI CO SE ZMĚNILO:
- Najdi soubory modifikované za posledních 7 dní:
  find /Users/mb/Documents/KAUZA_TJ_KRUPKA_obsidian -name "*.md" -newer /Users/mb/Documents/KAUZA_TJ_KRUPKA_obsidian/15_System/AI_Review_Prompt.md -type f
- Zkontroluj nové soubory (přidané od poslední kontroly)
- Přečti UKOLY_A_STAV.md a identifikuj splněné úkoly
- Přečti LOG ZMĚN v dashboardu

KROK 2 — IDENTIFIKUJ DOPADY:
Pro každý nový nebo změněný soubor urči:
a) Jaké přehledy (dashboardy) jsou ovlivněny?
b) Jaké záznamy (osoby, org., události) je potřeba aktualizovat?
c) Jaká nová tvrzení nebo důkazy je potřeba přidat?
d) Jaké úkoly jsou splněny nebo nové?

KROK 3 — DOUBLE-CHECK:
Před navržením změn ověř:
- Neodporuje navrhovaná změna existujícím záznamům?
- Je změna doložena konkrétním dokumentem nebo skutečností?
- Neduplicuješ existující záznamy?

KROK 4 — NAVRHNI ZMĚNY (přehled po přehledu):
Prezentuj návrhy ODDĚLENĚ pro každý přehled v tomto pořadí:
1. UKOLY_A_STAV.md
2. Hlavni_Dashboard.md  
3. Casova_Osa (CAS-2026-001)
4. Osoby — záznamy k aktualizaci
5. Dokumenty — záznamy k aktualizaci
6. Tvrzení — nová nebo ke změně stavu
7. Události — nové nebo k aktualizaci

Pro každý přehled:
- Uveď CO se mění a PROČ (odkaz na konkrétní soubor/fakt)
- Čekej na potvrzení před dalším přehledem
- Po potvrzení proveď změnu a zaznamenej do LOG ZMĚN

FORMÁT NÁVRHU:
---
NÁVRH PRO: [název přehledu]
Změna: [co přidat/změnit/smazat]
Důvod: [proč — odkaz na dokument]
Dopad: [co to znamená pro kauzu]
Potvrdit? [ANO / NE / UPRAVIT]
---
```

---

## SEKCE 2 — CHECKLIST PŘEHLEDŮ (pro ruční kontrolu)

Po každém review zaškrtněte, které přehledy byly zkontrolovány a potvrzeny:

### Hlavní dashboardy
- [ ] `14_Dashboard/UKOLY_A_STAV.md` — úkoly a stavy
- [ ] `14_Dashboard/Hlavni_Dashboard.md` — statistiky a novinky
- [ ] `14_Dashboard/Osoby_Prehled.md` — přehled osob
- [ ] `14_Dashboard/Organizace_Prehled.md` — přehled organizací
- [ ] `14_Dashboard/Dukazy_Prehled.md` — přehled důkazů
- [ ] `14_Dashboard/Tvrzeni_Prehled.md` — přehled tvrzení
- [ ] `14_Dashboard/Dokumenty_Prehled.md` — přehled dokumentů
- [ ] `14_Dashboard/Casova_Osa_Prehled.md` — časová osa
- [ ] `14_Dashboard/Udalosti_Prehled.md` — přehled událostí

### Klíčové záznamy
- [ ] `06_Casova_Osa/CAS-2026-001_Casova_Osa_TJK_2021_2026.md` — doplnit nové události
- [ ] `15_System/Identifikatory.md` — nové ID
- [ ] `09_Vystupy/AUDIT_REPORT_2026-06-18.md` — zastaralé?
- [ ] `09_Vystupy/IMPORT_KRITICKA_PRIORITA_REPORT.md` — zastaralé?

---

## SEKCE 3 — POTVRDIT ZMĚNY (log potvrzení)

| Datum | Přehled | Změna | Potvrdil | Status |
|-------|---------|-------|---------|--------|
| 2026-06-21 | UKOLY_A_STAV | Vytvoření dashboardu | — | ✅ Vytvořeno |
| | | | | |

> [!NOTE] Jak zaznamenat potvrzení
> Po každém potvrzení přidejte řádek do tabulky výše.
> Formát: `Datum | Přehled | Popis změny | Vaše jméno/initials | ✅`

---

## SEKCE 4 — PRAVIDLA PRO AI REVIEW

### Co AI SMÍ navrhnout bez potvrzení:
- Doplnění chybějícího ID do registru
- Oprava překlepu v metadata
- Přidání odkazu na existující soubor

### Co AI MUSÍ čekat na potvrzení:
- Změna stavu tvrzení (neovereno → podlozeno atd.)
- Přidání nové osoby nebo organizace
- Změna stavu úkolu (splněno/nesplněno)
- Aktualizace přehledů a dashboardů
- Jakákoliv změna v soudních řízeních (sp. zn., výsledky)

### Zakázané akce (nikdy bez explicitního příkazu):
- Mazání existujících záznamů
- Přesun nebo přejmenování souborů
- Změna obsahu důkazních dokumentů
- Přidání právních závěrů (AI neurčuje vinu)

---

## SEKCE 5 — QUICK STATUS COMMANDS

Spusťte tyto příkazy pro rychlý přehled stavu:

### Nové soubory (posledních 7 dní)
```bash
find /Users/mb/Documents/KAUZA_TJ_KRUPKA_obsidian -name "*.md" -newer /Users/mb/Documents/KAUZA_TJ_KRUPKA_obsidian/START_HERE.md -not -path "*/.obsidian/*" | sort
```

### Naposledy změněné soubory
```bash
find /Users/mb/Documents/KAUZA_TJ_KRUPKA_obsidian -name "*.md" -not -path "*/.obsidian/*" | xargs ls -lt | head -20
```

### Počet záznamů podle typu
```bash
for dir in 01_Osoby 02_Organizace 03_Udalosti 04_Dukazy 05_Dokumenty 07_Tvrzeni 08_Analyzy 10_Pravni_Podklady; do echo "$dir: $(ls /Users/mb/Documents/KAUZA_TJ_KRUPKA_obsidian/$dir/*.md 2>/dev/null | wc -l)"; done
```

### Otevřené checkboxy (úkoly)
```bash
grep -r "^- \[ \]" /Users/mb/Documents/KAUZA_TJ_KRUPKA_obsidian --include="*.md" | wc -l
```
