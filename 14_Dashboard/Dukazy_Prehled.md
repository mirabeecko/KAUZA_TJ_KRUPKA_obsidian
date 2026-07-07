---
typ: prehled
nazev: Přehled důkazů
tagy:
  - prehled
  - dukazy
---

# Přehled důkazů

## Všechny důkazy

```dataview
TABLE id, datum, typ, kategorie, zdroj, stav_dukazu, pravni_hodnota
FROM "04_Dukazy"
WHERE typ = "dukaz"
SORT datum DESC
```

## Důkazy podle kategorie

```dataview
TABLE id, datum, zdroj, stav_dukazu
FROM "04_Dukazy"
WHERE typ = "dukaz"
GROUP BY kategorie
SORT datum DESC
```

## Neověřené důkazy

```dataview
TABLE id, datum, typ, zdroj, popis
FROM "04_Dukazy"
WHERE stav_dukazu = "neoveren"
SORT datum DESC
```

## Důkazy bez vazeb

```dataview
TABLE id, datum, typ, popis
FROM "04_Dukazy"
WHERE !osoby AND !organizace AND !udalosti
```

## Důkazy bez hash (integrita nezajištěna)

```dataview
TABLE id, datum, typ, soubor
FROM "04_Dukazy"
WHERE soubor AND !hash_sha256
SORT datum DESC
```

## Důkazy podle osob

```dataview
TABLE id, datum, typ, stav_dukazu
FROM "04_Dukazy"
WHERE typ = "dukaz"
GROUP BY osoby
```

## Důkazy podle organizací

```dataview
TABLE id, datum, typ, stav_dukazu
FROM "04_Dukazy"
WHERE typ = "dukaz"
GROUP BY organizace
```

## Přehled importovaných důkazů (s odkazy na soubory)

```dataviewjs
const pages = dv.pages('"04_Dukazy"').where(p => p.typ == "dukaz").sort(p => p.datum, 'desc');
const rows = pages.map(p => {
    const id = p.id || "—";
    const datum = p.datum || "—";
    const kategorie = p.kategorie || "—";
    const stav = p.stav_dukazu || "—";
    const nazev = p.file.name;
    const odkaz = p.odkaz ? p.odkaz : (p.soubor ? "[📎 soubor](file://" + encodeURI(p.soubor) + ")" : "—");
    return [id, datum, kategorie, stav, nazev, odkaz];
});
dv.table(["ID", "Datum", "Kategorie", "Stav", "Poznámka", "Soubor"], rows);
```

> 💡 **Tip:** Sloupec **Poznámka** obsahuje název poznámky v Obsidianu — kliknutím ji otevřete. Sloupec **Soubor** obsahuje přímý odkaz na původní dokument v počítači / Google Drive.
