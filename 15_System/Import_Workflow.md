---
typ: system
nazev: Importní workflow
tagy:
  - system
  - workflow
  - import
---

# Importní workflow

## Přehled

Všechny nové soubory vkládejte nejprve do složky `12_Import/`.

## Podporované typy souborů

| Typ | Postup zpracování |
|-----|------------------|
| PDF | OCR + extrakce textu → AI analýza |
| DOCX/DOC | Přímé čtení → AI analýza |
| TXT | Přímé čtení → AI analýza |
| EML/MSG | Extrakce záhlaví + těla → AI analýza |
| JPG/PNG | OCR nebo ruční popis → AI analýza |
| MP4/MP3 | Transkripce → AI analýza |
| XLS/XLSX | Extrakce dat → AI analýza |

---

## Krok za krokem

### Krok 1 — Příjem dokumentu

- [ ] Uložte soubor do `12_Import/`
- [ ] Pojmenujte soubor: `RRRR-MM-DD_popis.přípona`
- [ ] Zaznamenejte: datum získání, zdroj, způsob získání

### Krok 2 — Předběžné zhodnocení

Zodpovězte tyto otázky:
- [ ] O čem dokument pojednává?
- [ ] Jaký je jeho typ? (smlouva, korespondence, rozhodnutí, faktura...)
- [ ] Jaké je přibližné datum vzniku?
- [ ] Kdo je autor/vydavatel?
- [ ] Kdo je příjemce?
- [ ] Jak byl dokument získán?

### Krok 3 — AI analýza

Použijte prompt **č. 1 — ANALÝZA DOKUMENTU** z [[AI_Prompty]]:

1. Zkopírujte obsah dokumentu nebo jeho popis
2. Vložte do AI asistenta s promptem č. 1
3. Výstup použijte pro vyplnění záznamu

### Krok 4a — Vytvoření záznamu Dokument

- [ ] Otevřete šablonu `13_Sablony/Dokument.md`
- [ ] Vytvořte nový soubor v `05_Dokumenty/`
- [ ] Pojmenujte: `DOK-RRRR-NNN_nazev.md`
- [ ] Vyplňte YAML frontmatter (id, typ, kategorie, datum, autor...)
- [ ] Doplňte popis a klíčové pasáže
- [ ] Přesuňte originální soubor do `05_Dokumenty/prilohy/`
- [ ] Zaregistrujte ID v [[Identifikatory]]

### Krok 4b — Vytvoření záznamu Důkaz (pokud relevantní)

- [ ] Otevřete šablonu `13_Sablony/Dukaz.md`
- [ ] Vytvořte nový soubor v `04_Dukazy/`
- [ ] Pojmenujte: `DUK-RRRR-NNN_nazev.md`
- [ ] Vyplňte metadata včetně hash souborů
- [ ] Zaznamenejte chain of custody
- [ ] Zaregistrujte ID v [[Identifikatory]]

### Krok 5 — Extrakce entit

#### Osoby

- [ ] Pro každou zmíněnou osobu: hledat v `01_Osoby/`
- [ ] Pokud neexistuje: vytvořit ze šablony `Osoba.md`
- [ ] Přidat odkaz na nový dokument do záznamu osoby
- [ ] Zaregistrovat nové ID v [[Identifikatory]]

#### Organizace

- [ ] Pro každou zmíněnou organizaci: hledat v `02_Organizace/`
- [ ] Pokud neexistuje: vytvořit ze šablony `Organizace.md`
- [ ] Ověřit IČO v [ARES](https://ares.gov.cz)
- [ ] Zaregistrovat nové ID v [[Identifikatory]]

#### Události

- [ ] Identifikovat popsané události
- [ ] Hledat existující záznamy v `03_Udalosti/`
- [ ] Pokud neexistují: vytvořit ze šablony `Udalost.md`
- [ ] Zaregistrovat nové ID v [[Identifikatory]]

### Krok 6 — Vzájemné propojení

- [ ] Aktualizovat záznamy osob (přidat `[[wikilink]]` na dokument)
- [ ] Aktualizovat záznamy organizací
- [ ] Aktualizovat záznamy událostí
- [ ] Doplnit YAML pole `osoby:`, `organizace:`, `udalosti:` ve všech relevantních záznamech

### Krok 7 — Tvrzení

- [ ] Identifikovat tvrzení obsažená v dokumentu
- [ ] Hledat existující záznamy v `07_Tvrzeni/`
- [ ] Nová tvrzení: vytvořit ze šablony `Tvrzeni.md`
- [ ] Propojit důkazy s tvrzeními (`podpora_dukazy:` / `vyvraceni_dukazy:`)
- [ ] Zaregistrovat nová ID v [[Identifikatory]]

### Krok 8 — Finalizace

- [ ] Přesunout zpracovaný soubor z `12_Import/` na finální místo
- [ ] Zkontrolovat, že Dashboard zobrazuje nové záznamy
- [ ] Poznamenat do [[../00_Inbox/|Inboxu]] případné otevřené otázky

### Krok 9 — Aktualizace živého shrnutí kauzy (volitelné, doporučeno)

> [!TIP] Tento krok proveďte, pokud nový import mění celkový obraz kauzy.

- [ ] Spusťte AI prompt č. 13 — AKTUALIZACE ŽIVÉHO SHRNUTÍ KAUZY
- [ ] AI aktualizuje soubor `09_Vystupy/ZIVE_SHRNUTI_KAUZY.md`
- [ ] **PŘEČTĚTE** vygenerovaný text — zkontrolujte fakta a odstraňte halucinace
- [ ] Schválte: změňte `status_revize:` na `schvaleno` a aktualizujte `datum_posledni_aktualizace`
- [ ] Nebo opravte: upravte text ručně a změňte `status_revize:` na `opraveno_clovekem`

**Pravidlo:** Živé shrnutí se aktualizuje jen při významné změně kontextu, ne po každém importu.

---

## Systém identifikátorů

| Typ | Formát | Příklad |
|-----|--------|---------|
| Osoba | OSO-RRRR-NNN | OSO-2024-001 |
| Organizace | ORG-RRRR-NNN | ORG-2023-012 |
| Událost | UDA-RRRR-NNN | UDA-2024-003 |
| Důkaz | DUK-RRRR-NNN | DUK-2024-047 |
| Dokument | DOK-RRRR-NNN | DOK-2023-008 |
| Tvrzení | TVR-RRRR-NNN | TVR-2024-002 |
| Analýza | ANL-RRRR-NNN | ANL-2024-001 |
| Právní podklad | PRP-RRRR-NNN | PRP-2024-001 |
| Mediální výstup | MED-RRRR-NNN | MED-2024-015 |

**RRRR** = rok přidání do systému (ne rok vzniku dokumentu)  
**NNN** = pořadové číslo v roce: 001, 002, 003...

---

## Složky pro přílohy

```
04_Dukazy/prilohy/     — originální soubory důkazů
05_Dokumenty/prilohy/  — originální soubory dokumentů
11_Media/prilohy/      — mediální soubory
```

---

## Integrita důkazů

> [!CAUTION] Zachování integrity
> U klíčových důkazů vždy zaznamenejte:
> - **Hash souboru**: MD5 a SHA-256
> - **Datum a způsob získání**
> - **Chain of custody**: kdo s důkazem zacházel a kdy
> - **Místo uložení originálu**

Výpočet hash na macOS:
```bash
md5 soubor.pdf
shasum -a 256 soubor.pdf
```
