---
id: OSO-RRRR-NNN
typ: osoba
cele_jmeno: 
jmeno: 
prijmeni: 
narozeni: 
umrti: 
pohlavi: 
narodnost: česká
role: []
organizace: []
kontakt_email: 
kontakt_telefon: 
kontakt_adresa: 
kontakt_datova_schranka: 
popis: 
stav: aktivni
relevance: stredni
porusene_zakony: []
instituce: []
duvernost: interni
vytvoreno: 2026-06-18
upraveno: 2026-06-18
tagy:
  - osoba
---

# Jméno Příjmení

## Základní identifikace

| Pole | Hodnota |
|------|---------|
| **ID** | OSO-RRRR-NNN |
| **Celé jméno** | |
| **Role** | |
| **Organizace** | |
| **Datum narození** | |
| **Stav** | aktivní |
| **Porušené zákony** | |
| **Instituce** | |

## Popis a charakteristika

> [!NOTE] Přehled osoby
> Stručný popis osoby a její role v případu.

## Kontaktní informace

- **E-mail:** 
- **Telefon:** 
- **Adresa:** 
- **Datová schránka:** 

## Vazby na organizace

```dataview
TABLE id, nazev, role_osoby
FROM "02_Organizace"
WHERE contains(osoby, this.file.name)
SORT nazev ASC
```

## Události, na nichž se podílela

```dataview
TABLE datum, popis, misto
FROM "03_Udalosti"
WHERE contains(osoby, this.file.name)
SORT datum ASC
```

## Dokumenty

```dataview
TABLE datum, typ, nazev
FROM "05_Dokumenty"
WHERE contains(autor, this.file.name) OR contains(osoby, this.file.name)
SORT datum DESC
```

## Důkazy

```dataview
TABLE datum, typ, zdroj, stav_dukazu
FROM "04_Dukazy"
WHERE contains(osoby, this.file.name)
SORT datum DESC
```

## Tvrzení

```dataview
TABLE text_tvrzeni, stav, podpora_dukazy
FROM "07_Tvrzeni"
WHERE contains(osoby, this.file.name)
SORT stav ASC
```

## Chronologická osa aktivity

```dataview
TABLE datum, typ, popis
FROM "03_Udalosti", "04_Dukazy", "05_Dokumenty"
WHERE contains(osoby, this.file.name)
SORT datum ASC
```

## Analytické poznámky

> [!WARNING] Upozornění
> Obsah této sekce jsou analytické hypotézy — **ne fakta ani závěry**.

## Otevřené otázky

- [ ] 

## Zdroje a reference

- 

## Související záznamy

- 
