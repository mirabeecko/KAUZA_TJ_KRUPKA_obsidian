---
typ: navod
nazev: START HERE — Průvodce systémem
tagy:
  - navod
  - system
---

# Analytický znalostní systém — Průvodce

> [!IMPORTANT] Systémové upozornění
> Tento systém slouží k analytické práci s dokumenty a důkazy.
> **AI neurčuje vinu ani pravdivost tvrzení.**
> AI pomáhá identifikovat vazby, rozpory a chybějící důkazy.
> Fakta, tvrzení, důkazy a hypotézy jsou vždy striktně odděleny.

---

> [!tip] 🏠 HLAVNÍ ROZCESTNÍK
> Pro rychlou navigaci kauzou použijte **[[⤴️ 🏠 ROZCESTNÍK]]** — vizuální rozcestník s přehledem aktuálního stavu, všemi sekcemi a mapou vazeb.

---

## Rychlý start

### 1. Otevřete Rozcestník nebo Dashboard

→ [[⤴️ 🏠 ROZCESTNÍK|🏠 Hlavní rozcestník]] ← **DOPORUČENÝ VSTUPNÍ BOD**

→ [[14_Dashboard/Hlavni_Dashboard|📊 Dashboard]] (technický přehled s Dataview dotazy)

Dashboard/rozcestník zobrazuje celkový přehled systému, nejnovější záznamy a otevřené otázky.

### 2. Přidejte nový dokument

1. Vložte soubor do složky `12_Import/`
2. Otevřete [[15_System/Import_Workflow]] a postupujte podle kroků
3. Použijte AI prompt z [[15_System/AI_Prompty]] pro rychlou analýzu

### 3. Vytvořte záznamy

Šablony jsou ve složce `13_Sablony/`. Pro každý typ entity:

| Co přidávám | Šablona | Cílová složka |
|-------------|---------|--------------|
| Nová osoba | [[13_Sablony/Osoba]] | `01_Osoby/` |
| Nová organizace | [[13_Sablony/Organizace]] | `02_Organizace/` |
| Nová událost | [[13_Sablony/Udalost]] | `03_Udalosti/` |
| Nový důkaz | [[13_Sablony/Dukaz]] | `04_Dukazy/` |
| Nový dokument | [[13_Sablony/Dokument]] | `05_Dokumenty/` |
| Nové tvrzení | [[13_Sablony/Tvrzeni]] | `07_Tvrzeni/` |
| Nová analýza | [[13_Sablony/Analyza]] | `08_Analyzy/` |
| Právní podklad | [[13_Sablony/Pravni_Podklad]] | `10_Pravni_Podklady/` |
| Mediální výstup | [[13_Sablony/Medialni_Vystup]] | `11_Media/` |

---

## Struktura systému

```
KAUZA_TJ_KRUPKA_obsidian/
│
├── 00_Inbox/           ← Dočasné poznámky a nezpracované nápady
├── 01_Osoby/           ← Záznamy o osobách
├── 02_Organizace/      ← Záznamy o organizacích
├── 03_Udalosti/        ← Záznamy o událostech
├── 04_Dukazy/          ← Záznamy o důkazech + originály v prilohy/
├── 05_Dokumenty/       ← Záznamy o dokumentech + originály v prilohy/
├── 06_Casova_Osa/      ← Speciální nebo ruční časové osy
├── 07_Tvrzeni/         ← Záznamy o tvrzeních
├── 08_Analyzy/         ← Analytické zprávy
├── 09_Vystupy/         ← Finální výstupy a zprávy
├── 10_Pravni_Podklady/ ← Podklady pro právníky, úřady, policii, SZ
├── 11_Media/           ← Mediální výstupy a sledování médií
├── 12_Import/          ← SEM VKLÁDEJTE NOVÉ SOUBORY
├── 13_Sablony/         ← Šablony pro všechny typy záznamů
├── 14_Dashboard/       ← Přehledy a dashboardy (Dataview)
└── 15_System/          ← Systémová dokumentace a konfigurace
```

---

## Datový model

### Typy záznamů a identifikátory

| Typ | ID formát | Příklad | Složka |
|-----|-----------|---------|--------|
| Osoba | OSO-RRRR-NNN | OSO-2024-001 | 01_Osoby/ |
| Organizace | ORG-RRRR-NNN | ORG-2023-012 | 02_Organizace/ |
| Událost | UDA-RRRR-NNN | UDA-2024-003 | 03_Udalosti/ |
| Důkaz | DUK-RRRR-NNN | DUK-2024-047 | 04_Dukazy/ |
| Dokument | DOK-RRRR-NNN | DOK-2023-008 | 05_Dokumenty/ |
| Tvrzení | TVR-RRRR-NNN | TVR-2024-002 | 07_Tvrzeni/ |
| Analýza | ANL-RRRR-NNN | ANL-2024-001 | 08_Analyzy/ |
| Právní podklad | PRP-RRRR-NNN | PRP-2024-001 | 10_Pravni_Podklady/ |
| Mediální výstup | MED-RRRR-NNN | MED-2024-015 | 11_Media/ |

### Stavy tvrzení

| Stav (YAML hodnota) | Popis |
|--------------------|-------|
| `neovereno` | Žádné důkazy pro ani proti |
| `castecne_podlozeno` | Existují podporující důkazy, ale nedostatečné |
| `podlozeno` | Silné podporující důkazy |
| `vyvraceno` | Důkazy tvrzení vyvracejí |

### Stavy důkazů

| Stav (YAML hodnota) | Popis |
|--------------------|-------|
| `neoveren` | Autenticita nezkoumána |
| `overen` | Autenticita potvrzena |
| `zpochybneny` | Zpochybněna autenticita nebo hodnota |
| `nerelevantni` | Relevance pro případ vyloučena |

---

## Zásadní pravidla

> [!WARNING] Tato pravidla jsou závazná pro správnou analytickou práci

1. **Odděluj fakta od hypotéz** — vždy jasně označuj, co je doložené a co je domněnka
2. **Neuroč vinu** — systém slouží k organizaci informací, ne k právním závěrům
3. **Vše propojuj** — každý záznam musí být propojen přes `[[wikilink]]` s relevatními záznamy
4. **Zachovávej integritu důkazů** — u klíčových důkazů vždy zaznamenej chain of custody a hash
5. **Aktualizuj záznamy** — při každé nové informaci aktualizuj datum `upraveno:` a obsah
6. **Registruj ID** — každé přidělené ID zaznamenej v [[15_System/Identifikatory]] předem

---

## Workflow pro různé situace

### Přišel nový dokument

```
12_Import/ → AI analýza (prompt č. 1)
          → 05_Dokumenty/ (záznam DOK-)
          → 04_Dukazy/ (pokud důkaz, záznam DUK-)
          → aktualizace 01_Osoby/ a 02_Organizace/
          → vytvoření/aktualizace 07_Tvrzeni/
          → Dashboard se aktualizuje automaticky přes Dataview
```

### Příprava pro právníka

```
Shromáždění materiálů → AI prompt č. 7
                      → 10_Pravni_Podklady/ (záznam PRP-)
                      → 09_Vystupy/ (finální verze)
```

### Příprava podnětu na policii

```
07_Tvrzeni/ + 04_Dukazy/ → AI prompt č. 8
                          → 10_Pravni_Podklady/ (záznam PRP-)
                          → 09_Vystupy/ (finální verze)
```

### Příprava podnětu státnímu zastupitelství

```
Vše relevantní → AI prompt č. 12
              → 10_Pravni_Podklady/ (záznam PRP-)
              → 09_Vystupy/ (finální verze s paginací)
```

### Hluboká analýza

```
Shromáždění dat → AI prompty č. 2-6
               → 08_Analyzy/ (záznam ANL-)
               → závěry do 09_Vystupy/
```

---

## AI analytické prompty

Všechny prompty v [[15_System/AI_Prompty]]:

| Č. | Prompt | Kdy použít |
|----|--------|-----------|
| 1 | Analýza dokumentu | Při každém novém dokumentu |
| 2 | Analýza osoby | Pro hloubkový profil osoby |
| 3 | Analýza organizace | Pro hloubkový profil organizace |
| 4 | Analýza časové osy | Pro chronologický přehled |
| 5 | Hledání rozporů | Při srovnávání tvrzení a zdrojů |
| 6 | Chybějící důkazy | Pro identifikaci mezer |
| 7 | Podklady pro právníka | Příprava konzultace |
| 8 | Podklady pro policii | Příprava trestního oznámení |
| 9 | Podklady pro úřad | Správní podání |
| 10 | Souhrnná analytická zpráva | Celkové shrnutí případu |
| 11 | Kontrola záznamu | Ověření úplnosti záznamu |
| 12 | Podnět státnímu zastupitelství | Příprava podnětu SZ |

---

## Graf vztahů

Otevřete **Graph View** (`Ctrl+G` nebo `Cmd+G`) pro vizualizaci vztahů.

Každý záznam propojený přes `[[wikilink]]` se zobrazí jako uzel v grafu. Čím více vazeb záznam má, tím centrálnější uzel v grafu bude.

**Nastavení barevných skupin** v Graph View → Groups:

| Cesta | Barva |
|-------|-------|
| `01_Osoby` | červená |
| `02_Organizace` | modrá |
| `03_Udalosti` | zelená |
| `04_Dukazy` | oranžová |
| `05_Dokumenty` | šedá |
| `07_Tvrzeni` | fialová |
| `08_Analyzy` | žlutá |

---

## Přehledy a dashboardy

| Přehled | Soubor |
|---------|--------|
| Hlavní dashboard | [[14_Dashboard/Hlavni_Dashboard]] |
| Osoby | [[14_Dashboard/Osoby_Prehled]] |
| Organizace | [[14_Dashboard/Organizace_Prehled]] |
| Události | [[14_Dashboard/Udalosti_Prehled]] |
| Důkazy | [[14_Dashboard/Dukazy_Prehled]] |
| Dokumenty | [[14_Dashboard/Dokumenty_Prehled]] |
| Tvrzení | [[14_Dashboard/Tvrzeni_Prehled]] |
| Časová osa | [[14_Dashboard/Casova_Osa_Prehled]] |

---

## Potřebné pluginy (instalace)

Systém vyžaduje plugin **Dataview** — bez něj přehledy nefungují.

1. Obsidian → Nastavení → Komunitní pluginy → Procházet
2. Hledat: `Dataview` → Instalovat → Zapnout
3. Hledat: `Templater` → Instalovat → Zapnout
4. V nastavení Templater nastavit: Template folder = `13_Sablony`

Viz [[15_System/Konfigurace]] pro kompletní seznam a nastavení.

---

## Bezpečnost

> [!CAUTION] Citlivé informace
> - Vault může obsahovat citlivé právní a osobní informace
> - Povolte šifrování disku: **FileVault** na macOS
> - Zálohy pouze na šifrovaná úložiště
> - Nikdy nesdílejte vault přes nešifrované kanály (email, Dropbox bez šifrování)
> - Před sdílením s třetí stranou konzultujte s právníkem

Zálohovací strategie: viz [[15_System/Konfigurace]]

---

*Systém vytvořen: 2026-06-18*  
*Verze: 1.0*
