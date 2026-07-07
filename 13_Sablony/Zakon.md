---
id: <% tp.file.title.split("_")[0] %>
typ: zakon
nazev: 
cislo_zakona: 
rok_vydani: 
ucinnost_od: 
stav: aktivni
sankce:
  - trestni
  - spravni
  - civilni
tagy:
  - zakon
  - pravni_predpis
---

# <% tp.file.title %>

> [!INFO] Základní údaje
> | Parametr | Hodnota |
> |----------|---------|
> | **Číslo zákona** | |
> | **Rok vydání** | |
> | **Účinnost od** | |
> | **Stav** | aktivní |

## Účel a rozsah působnosti

*[Stručný popis účelu zákona a jeho působnosti — doplnit dle potřeby]*

## Použité paragrafy v kauze TJK

> [!IMPORTANT] Seznam paragrafů
> Níže jsou uvedeny pouze paragrafy, které se přímo vyskytují v dokumentaci kauzy TJK. Pro úplné znění zákona použijte oficiální zdroj (např. zakonyprolidi.cz).

---

## § 1 — *[Název paragrafu]*

> [!WARNING] Znění ke kontrole
> Znění paragrafu je uvedeno v aktuální podobě k datu vytvoření. Doporučeno ověřit v aktuálním znění zákona.

*[Zde vložit znění paragrafu]*

### Související dokumenty v kauze

- [[DOkument]] — odkaz na dokument, kde je paragraf použit

---

## Přehled odkazů z kauzy

```dataview
TABLE nazev AS "Název", datum AS "Datum"
FROM ""
WHERE contains(file.outlinks, this.file.link)
SORT datum ASC
```

## Externí zdroje

- [zakonyprolidi.cz](https://www.zakonyprolidi.cz/) — aktuální znění zákonů
- [Sbírka zákonů](https://www.e-sbirka.cz/) — oficiální znění

## Tagy

#zakon #pravni_predpis
