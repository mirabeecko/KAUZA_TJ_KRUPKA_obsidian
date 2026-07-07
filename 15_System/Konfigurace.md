---
typ: system
nazev: Konfigurace systému
tagy:
  - system
  - konfigurace
---

# Konfigurace systému

## Doporučené pluginy pro Obsidian

### Nezbytné

| Plugin | Účel | Klíčové nastavení |
|--------|------|------------------|
| **Dataview** | Automatické přehledy a tabulky | Povolit JavaScript Queries |
| **Templater** | Šablony s dynamickými poli | Složka šablon: `13_Sablony` |

### Doporučené

| Plugin                     | Účel                                         |
| -------------------------- | -------------------------------------------- |
| **Tasks**                  | Správa checklistů a úkolů ve všech souborech |
| **Calendar**               | Navigace podle data                          |
| **Graph Analysis**         | Pokročilá analýza grafu vztahů               |
| **Strange New Worlds**     | Zobrazení zpětných odkazů inline             |
| **Folder Note**            | Přehledová stránka pro každou složku         |
| **Tag Wrangler**           | Správa a přejmenování tagů                   |
| **Obsidian Git**           | Automatická záloha do Git repozitáře         |
| **Natural Language Dates** | Zadávání dat přirozeným jazykem              |
| **Kanban**                 | Kanban pohled pro správu workflow            |

---

## Konfigurace Dataview

V nastavení pluginu Dataview povolte:
- **Enable JavaScript Queries**: zapnuto
- **Enable Inline Queries**: zapnuto
- **Date format**: `YYYY-MM-DD`
- **Inline Query Prefix**: `=`

---

## Konfigurace Templater

- **Template folder location**: `13_Sablony`
- **Trigger Templater on new file creation**: zapnuto
- **Enable Folder Templates**: volitelně

---

## Konfigurace Graph View (graf vztahů)

Nastavení pro vizualizaci vztahů v Obsidian Graph View:

### Barevné skupiny

| Složka | Barva | Typ entity |
|--------|-------|-----------|
| `01_Osoby` | červená | Osoby |
| `02_Organizace` | modrá | Organizace |
| `03_Udalosti` | zelená | Události |
| `04_Dukazy` | oranžová | Důkazy |
| `05_Dokumenty` | šedá | Dokumenty |
| `07_Tvrzeni` | fialová | Tvrzení |
| `08_Analyzy` | žlutá | Analýzy |
| `14_Dashboard` | bílá | Přehledy |
| `16_Zakony` | fialová | Zákony |

### Doporučené filtry

- Skrýt složky: `13_Sablony`, `15_System`
- Zobrazit pouze: soubory s vazbami (min. 1 odkaz)

---

## Stupně důvěrnosti

| Stupeň | Hodnota v YAML | Popis |
|--------|---------------|-------|
| 1 | `verejne` | Veřejně dostupné informace |
| 2 | `interni` | Interní pracovní materiály |
| 3 | `konfidencialni` | Důvěrné — sdílet pouze s právníkem |
| 4 | `tajne` | Maximální ochrana |

---

## Zálohovací strategie

1. **Lokální záloha (Git)**: Obsidian Git plugin → automatický commit každou hodinu do privátního repozitáře
2. **Šifrovaná záloha**: Minimálně týdně na šifrovaný externí disk
3. **Cloudová záloha**: Šifrovaný cloud (Tresorit, ProtonDrive, nebo iCloud s FileVault)

> [!CAUTION] Bezpečnost
> Obsah vaultu může obsahovat citlivé právní informace.
> Nikdy neukládejte vault na nešifrovaná úložiště.
> Povolte FileVault na macOS.

---

## Architektura pro budoucí rozšíření

### Plánované integrace

```yaml
claude_desktop:
  mcp_server: obsidian-mcp
  vault_path: /Users/mb/Documents/KAUZA_TJ_KRUPKA_obsidian
  schopnosti:
    - čtení a zápis poznámek přirozeným jazykem
    - automatická tvorba záznamů při importu
    - analytické dotazy napříč celým vaultem

qdrant:
  ucel: sémantické vyhledávání v dokumentech
  embeddingy: text-embedding-3-large
  kolekce:
    - dokumenty
    - tvrzeni
    - analyzy

postgresql:
  ucel: strukturovaná databáze pro velké objemy dat
  synchronizace: z Obsidian vault přes MCP

sqlite:
  ucel: lokální databáze pro rychlé dotazy offline

google_drive:
  ucel: záloha originálních dokumentů s verzováním

local_llm:
  ucel: offline analýza citlivých dokumentů
  modely:
    - ollama/llama3
    - ollama/mistral
    - lm-studio
```

### Napojení na Claude Desktop (MCP)

Po nastavení MCP serveru pro Obsidian bude možné:
- Klást dotazy na vault přirozeným jazykem
- Automaticky vytvářet záznamy z popisu
- Analyzovat dokumenty bez kopírování textu
- Hledat v grafu vztahů
- Generovat právní podklady na základě obsahu vaultu

### Sémantické vyhledávání s Qdrant

- Vložit obsah všech dokumentů jako embeddingy
- Hledat sémanticky podobné dokumenty
- Identifikovat tematicky propojené záznamy automaticky
- Klusterovat související tvrzení
