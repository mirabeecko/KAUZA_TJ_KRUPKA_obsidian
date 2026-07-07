---
typ: dashboard
nazev: Hlavní Dashboard
vytvoreno: 2026-06-18
tagy:
  - dashboard
  - system
---

# Analytický systém — Hlavní Dashboard

> [!IMPORTANT] Systémové upozornění
> Tento systém slouží ke správě důkazů a analytické práci.
> **AI neurčuje vinu ani pravdivost tvrzení.**
> AI pomáhá identifikovat vazby, rozpory a chybějící důkazy.

---

## Vizuální dashboard

> [!INFO] Excalidraw mapa kauzy
> Kliknutím otevřete vizuální přehled všech klíčových oblastí kauzy.

[[Hlavni_Dashboard.excalidraw|🗺️ Vizální dashboard v Excalidraw]]

---

## Statistiky systému

```dataview
TABLE WITHOUT ID
  "Typ" as Typ,
  length(rows) as Počet
FROM ""
WHERE typ
GROUP BY typ
SORT typ ASC
```

---

## Neověřená tvrzení

> [!CAUTION] Vyžadují pozornost

```dataview
TABLE id, text_tvrzeni, tvrditel, datum_tvrzeni, osoby
FROM "07_Tvrzeni"
WHERE stav = "neovereno"
SORT datum_tvrzeni DESC
```

---

## Tvrzení bez důkazů

```dataview
TABLE id, text_tvrzeni, stav, tvrditel
FROM "07_Tvrzeni"
WHERE !podpora_dukazy AND !vyvraceni_dukazy
SORT vytvoreno DESC
```

---

## Nejnovější důkazy

```dataview
TABLE id, datum, typ, zdroj, stav_dukazu
FROM "04_Dukazy"
WHERE typ = "dukaz"
SORT vytvoreno DESC
LIMIT 10
```

---

## Nejnovější dokumenty

```dataview
TABLE id, datum, kategorie, nazev, autor
FROM "05_Dokumenty"
WHERE typ = "dokument"
SORT datum DESC
LIMIT 10
```

---

## Poslední události

```dataview
TABLE id, datum, nazev, misto, osoby
FROM "03_Udalosti"
WHERE typ = "udalost"
SORT datum DESC
LIMIT 10
```

---

## Osoby (přehled)

```dataview
TABLE id, cele_jmeno, role, organizace, relevance
FROM "01_Osoby"
WHERE typ = "osoba"
SORT relevance DESC, prijmeni ASC
```

---

## Organizace (přehled)

```dataview
TABLE id, nazev, ico, pravni_forma, relevance
FROM "02_Organizace"
WHERE typ = "organizace"
SORT relevance DESC, nazev ASC
```

---

## Nevyřešené otázky

```dataview
TASK
FROM ""
WHERE !completed
SORT file.mtime DESC
LIMIT 20
```

---

## Chybějící vazby — důkazy bez zařazení

```dataview
TABLE id, datum, typ, popis
FROM "04_Dukazy"
WHERE !osoby AND !organizace AND !udalosti
SORT datum DESC
```

---

## Navigace

| Sekce | Odkaz |
|-------|-------|
| Osoby | [[../01_Osoby/|Složka Osoby]] |
| Organizace | [[../02_Organizace/|Složka Organizace]] |
| Události | [[../03_Udalosti/|Složka Události]] |
| Důkazy | [[../04_Dukazy/|Složka Důkazy]] |
| Dokumenty | [[../05_Dokumenty/|Složka Dokumenty]] |
| Časová osa | [[Casova_Osa_Prehled]] |
| Tvrzení | [[Tvrzeni_Prehled]] |
| Analýzy | [[../08_Analyzy/|Složka Analýzy]] |
| Klíčové události | [[../11_Klicove_Udalosti/INDEX_Klicove_Udalosti|Klíčové události]] |
| Shromáždění delegátů | [[../17_Schromazdeni_Delegatu/INDEX_Schromazdeni_Delegatu|Shromáždění delegátů]] |
| Výstupy | [[../09_Vystupy/|Složka Výstupy]] |
| Právní podklady | [[../10_Pravni_Podklady/|Složka Právní podklady]] |
| AI Prompty | [[../15_System/AI_Prompty]] |
| Import workflow | [[../15_System/Import_Workflow]] |
