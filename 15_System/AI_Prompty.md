---
typ: system
nazev: AI Prompty pro analytickou práci
tagy:
  - system
  - ai
  - prompty
---

# AI Prompty pro analytickou práci

> [!IMPORTANT] Jak používat tyto prompty
> Zkopírujte prompt, doplňte konkrétní data v hranatých závorkách `[...]` a odešlete do Claude nebo jiného AI asistenta.

---

## 1. ANALÝZA DOKUMENTU

```
Analyzuj následující dokument a proveď strukturovanou extrakci informací.

DOKUMENT:
[vložte obsah nebo popis dokumentu]

Proveď:
1. SHRNUTÍ: Stručné shrnutí obsahu (max 200 slov)
2. OSOBY: Vypiš všechny zmíněné osoby (jméno, role, kontext)
3. ORGANIZACE: Vypiš všechny zmíněné organizace (název, IČO pokud je uveden, kontext)
4. DATA A MÍSTA: Vypiš všechna data a místa s kontextem
5. KLÍČOVÁ TVRZENÍ: Vypiš tvrzení obsažená v dokumentu
6. ROZPORY: Identifikuj případné vnitřní rozpory
7. CHYBĚJÍCÍ INFORMACE: Co v dokumentu chybí nebo není vysvětleno?
8. PRÁVNÍ RELEVANCE: Jaká právní ustanovení mohou být relevantní?
9. DOPORUČENÍ: Jaké další informace by byly potřeba k ověření?

DŮLEŽITÉ: Nevyvozuj závěry o vině. Odděluj fakta od hypotéz.
```

---

## 2. ANALÝZA OSOBY

```
Proveď analytický profil osoby na základě dostupných informací.

OSOBA: [jméno osoby]

DOSTUPNÉ INFORMACE:
[vložte vše, co o osobě víte — dokumenty, tvrzení, události]

Proveď:
1. PROFIL: Základní profil osoby na základě doložených faktů
2. ROLE V PŘÍPADU: Jakou roli tato osoba hraje?
3. VAZBY: Identifikuj vazby na jiné osoby a organizace
4. CHRONOLOGIE: Sestavení časové osy aktivity osoby
5. TVRZENÍ O OSOBĚ: Shromáždi všechna tvrzení (kdo co tvrdí)
6. OVĚŘENÁ VS. NEOVĚŘENÁ FAKTA: Jasně oddělit
7. ROZPORY: Identifikuj rozpory ve výpovědích nebo chování
8. CHYBĚJÍCÍ INFORMACE: Co by bylo potřeba zjistit?
9. RIZIKA: Jaká rizika nebo otevřené otázky existují?

DŮLEŽITÉ: Nevyvozuj závěry o vině. Pracuj pouze s dostupnými informacemi.
```

---

## 3. ANALÝZA ORGANIZACE

```
Proveď analytický profil organizace na základě dostupných informací.

ORGANIZACE: [název organizace, IČO]

DOSTUPNÉ INFORMACE:
[vložte vše, co o organizaci víte]

Proveď:
1. PROFIL: Základní profil (právní forma, předmět činnosti, struktura)
2. VEDENÍ: Kdo organizaci řídí nebo řídil v relevantním období?
3. VAZBY: Vazby na jiné organizace a osoby
4. ROLE V PŘÍPADU: Jak se organizace případu týká?
5. DOKUMENTY: Jaké dokumenty od/o organizaci existují?
6. FINANČNÍ ASPEKTY: Relevantní finanční informace
7. VEŘEJNOPRÁVNÍ ZÁZNAMY: Co je dostupné z veřejných rejstříků?
8. ROZPORY: Identifikuj případné nesrovnalosti
9. CHYBĚJÍCÍ INFORMACE: Co by bylo potřeba ověřit?

DŮLEŽITÉ: Pracuj pouze s doloženými fakty.
```

---

## 4. ANALÝZA ČASOVÉ OSY

```
Proveď analýzu časové osy na základě dostupných dokumentů a informací.

DOSTUPNÉ UDÁLOSTI A DOKUMENTY:
[vložte chronologicky seřazené události nebo seznam dokumentů s daty]

Proveď:
1. REKONSTRUKCE: Sestavení chronologického přehledu
2. KLÍČOVÉ MILNÍKY: Identifikace klíčových bodů
3. MEZERY: Kde chybí informace nebo není jasné, co se dělo?
4. KAUZÁLNÍ VAZBY: Jaké události na sebe logicky navazují?
5. ANOMÁLIE: Co časově neodpovídá nebo je podezřelé?
6. KONFLIKTY: Kde si různé zdroje odporují v datech nebo pořadí?
7. PRESKRIPCE: Relevantní promlčecí lhůty nebo zákonné lhůty
8. DOPORUČENÍ: Jaké informace by vyplnily mezery?

DŮLEŽITÉ: Jasně označuj spekulace vs. doložená fakta.
```

---

## 5. HLEDÁNÍ ROZPORŮ

```
Analyzuj následující soubor informací a identifikuj všechny rozpory.

SOUBOR INFORMACÍ:
[vložte dokumenty, tvrzení, výpovědi]

Proveď:
1. INTERNÍ ROZPORY: Kde si jeden zdroj odporuje sám sobě?
2. KŘÍŽOVÉ ROZPORY: Kde si různé zdroje odporují navzájem?
3. ČASOVÉ ROZPORY: Kde data nebo pořadí událostí nedávají smysl?
4. FAKTICKÉ ROZPORY: Kde tvrzení odporují doloženým faktům?
5. LOGICKÉ ROZPORY: Co je logicky nemožné nebo nepravděpodobné?
6. HODNOCENÍ ZÁVAŽNOSTI: Které rozpory jsou klíčové pro případ?
7. MOŽNÁ VYSVĚTLENÍ: Jaká nevinná vysvětlení existují?
8. DOPORUČENÍ: Jak lze rozpory objasnit?

DŮLEŽITÉ: Neuváděj závěry o záměrnosti nebo vině.
```

---

## 6. HLEDÁNÍ CHYBĚJÍCÍCH DŮKAZŮ

```
Na základě dostupných informací identifikuj chybějící důkazy a mezery.

PŘÍPAD / HYPOTÉZA:
[popis situace nebo hypotézy, kterou chcete prověřit]

DOSTUPNÉ DŮKAZY:
[seznam dostupných důkazů]

Proveď:
1. MAPA DŮKAZŮ: Co je k dispozici a co chybí pro každé klíčové tvrzení?
2. KLÍČOVÉ MEZERY: Které chybějící důkazy jsou nejkritičtější?
3. ZDROJE: Kde by chybějící důkazy mohly existovat?
4. ZPŮSOBY ZÍSKÁNÍ: Jak lze tyto důkazy získat (svobodný přístup k informacím, rejstříky, svědci)?
5. RIZIKA ZTRÁTY: Které důkazy mohou být ohroženy (promlčení, likvidace)?
6. PRIORITIZACE: V jakém pořadí získávat chybějící důkazy?
7. ALTERNATIVNÍ DŮKAZY: Jak lze mezery obejít?

DŮLEŽITÉ: Absence důkazu není důkazem absence.
```

---

## 7. PŘÍPRAVA PODKLADŮ PRO PRÁVNÍKA

```
Připrav strukturovaný přehled pro konzultaci s právníkem.

KONTEXT PŘÍPADU:
[popis situace]

DOSTUPNÉ MATERIÁLY:
[seznam dostupných dokumentů a důkazů]

Připrav:
1. EXECUTIVE SUMMARY: Co se stalo (max 300 slov, pouze fakta)
2. KLÍČOVÉ OSOBY: Stručný přehled zúčastněných osob a jejich rolí
3. KLÍČOVÉ DOKUMENTY: Seznam a popis relevantních dokumentů
4. ČASOVÁ OSA: Chronologický přehled klíčových událostí
5. PRÁVNÍ OTÁZKY: Jaké právní otázky potřebují odpověď?
6. MOŽNÁ PRÁVNÍ RIZIKA: Identifikace právních rizik
7. OKAMŽITÉ KROKY: Co je třeba udělat nejdřív (promlčení, lhůty)?
8. OTEVŘENÉ OTÁZKY: Co potřebujete od právníka vědět?
9. PŘÍLOHY: Doporučené přílohy pro konzultaci

FORMÁT: Strukturovaný, přehledný dokument pro profesionální konzultaci.
```

---

## 8. PŘÍPRAVA PODKLADŮ PRO POLICII

```
Připrav strukturovaný podnět k prošetření pro Policii ČR.

KONTEXT:
[popis situace]

DOSTUPNÉ DŮKAZY:
[seznam důkazů]

Připrav:
1. POPIS SKUTKU: Přesný a faktický popis toho, co se stalo
2. MÍSTO A ČAS: Kde a kdy k tomu došlo
3. PODEZŘELÉ OSOBY: Kdo mohl být zapojen (bez označení viny)
4. SVĚDCI: Kdo může podávat výpověď
5. LISTINNÉ DŮKAZY: Přehled dokumentů pro předložení policii
6. VĚCNÉ DŮKAZY: Přehled fyzických důkazů
7. MOŽNÁ TRESTNÁ ČINNOST: Jaké trestné činy mohly být spáchány (paragraf zákona)
8. URGENTNOST: Proč je třeba jednat rychle (promlčení, hrozba zničení důkazů)
9. ŽÁDOST: Co žádáte policii, aby prošetřila

FORMÁT: Věcný, neutrální, bez emocionálního zabarvení.
```

---

## 9. PŘÍPRAVA PODKLADŮ PRO ÚŘAD / SPRÁVNÍ ŘÍZENÍ

```
Připrav podklady pro správní řízení nebo podání na úřad.

ÚŘAD: [název úřadu nebo instituce]
VĚC: [předmět podání]

DOSTUPNÉ MATERIÁLY:
[seznam dokumentů a informací]

Připrav:
1. IDENTIFIKACE ŽADATELE: Kdo podání podává
2. PŘEDMĚT PODÁNÍ: Co je požadováno nebo co se oznamuje
3. SKUTKOVÝ STAV: Přehled relevantních faktů
4. PRÁVNÍ ZÁKLAD: Relevantní zákony a ustanovení
5. DOKUMENTACE: Přehled přiložených dokladů
6. POŽADAVKY: Co konkrétně žadatel žádá
7. LHŮTY: Relevantní zákonné lhůty
8. FORMÁLNÍ NÁLEŽITOSTI: Podpis, datum, přílohy

FORMÁT: Formální administrativní styl, přehledná struktura.
```

---

## 10. PŘÍPRAVA SOUHRNNÉ ANALYTICKÉ ZPRÁVY

```
Připrav souhrnnou analytickou zprávu o případu.

PŘÍPAD:
[název nebo popis případu]

DOSTUPNÉ INFORMACE:
[shrnutí dostupných materiálů]

Připrav:
1. EXECUTIVE SUMMARY: Klíčová zjištění (max 500 slov)
2. METODOLOGIE: Jak byla analýza provedena, jaké jsou limity
3. PŘEHLED FAKTŮ: Prokázané skutečnosti s odkazem na zdroje
4. PŘEHLED HYPOTÉZ: Neověřená tvrzení a hypotézy
5. KLÍČOVÉ OSOBY: Stručný přehled s rolemi
6. KLÍČOVÉ ORGANIZACE: Přehled relevantních organizací
7. ČASOVÁ OSA: Chronologický přehled
8. ROZPORY: Identifikované nesrovnalosti
9. CHYBĚJÍCÍ DŮKAZY: Co schází a proč je to důležité
10. ZÁVĚR: Celkové analytické zhodnocení
11. DOPORUČENÍ: Navrhované další kroky
12. PŘÍLOHY: Přehled všech příloh

DŮLEŽITÉ: Jasně oddělit fakta od hypotéz. Neuvádět závěry o vině.
```

---

## 11. RYCHLÁ KONTROLA ZÁZNAMU

```
Zkontroluj kompletnost a integritu záznamu v systému.

ZÁZNAM:
[vložte obsah záznamu nebo jeho shrnutí]

Proveď:
1. CHYBĚJÍCÍ POLE: Která povinná pole nejsou vyplněna?
2. VAZBY: Jsou všechny vztahy správně propojeny?
3. KONZISTENCE: Jsou metadata konzistentní s obsahem?
4. DUPLICITY: Existují podobné záznamy v systému?
5. DOPORUČENÍ: Co doplnit nebo opravit?
```

---

## 12. PŘÍPRAVA PODNĚTU STÁTNÍMU ZASTUPITELSTVÍ

```
Připrav podnět k výkonu dohledu nebo trestní oznámení pro státní zastupitelství.

KONTEXT:
[popis situace]

DOSTUPNÉ MATERIÁLY:
[seznam dokumentů a důkazů]

Připrav:
1. ADRESÁT: Příslušné státní zastupitelství
2. PŘEDMĚT: Stručné shrnutí podnětu
3. SKUTKOVÝ STAV: Chronologický přehled faktů s odkazy na důkazy
4. PRÁVNÍ KVALIFIKACE: Možná trestná činnost (skutkové podstaty)
5. DŮKAZY: Strukturovaný přehled předkládaných důkazů
6. OSOBY: Přehled osob s popisem jejich rolí
7. PROCESNÍ ASPEKTY: Promlčení, příslušnost, urgentní opatření
8. NÁVRHY: Konkrétní procesní kroky k prošetření
9. PŘÍLOHY: Kompletní seznam příloh s paginací

FORMÁT: Formální právní styl, přesné citace, paginované přílohy.
```

---

## 13. AKTUALIZACE ŽIVÉHO SHRNUTÍ KAUZY

```
Na základě aktuálního stavu vaultu aktualizuj živé shrnutí kauzy.

AKTUÁLNÍ STAV VAULTU:
- Počet osob: [z dat]
- Počet událostí: [z dat]
- Počet dokumentů: [z dat]
- Počet důkazů: [z dat]
- Počet tvrzení: [z dat]

POSLEDNÍ ZMĚNY (od poslední revize shrnutí):
[vložte seznam nových záznamů, událostí, dokumentů]

Proveď:
1. EXECUTIVE SUMMARY — aktualizuj podle nových skutečností (max 400 slov)
2. STAV PŘÍPADU — aktualizuj tabulku milníků, přidej nové řádky
3. KLÍČOVÉ OSOBY — ověř, zda se změnily role nebo přibyly osoby
4. ČASOVÁ OSA — doplň nové milníky
5. OTEVŘENÉ OTÁZKY — posuň, vyřeš nebo přidej nová rizika
6. DŮKAZNÍ ZÁKLAD — aktualizuj statistiky
7. KONTEXT — přepiš, pokud se celkový směr kauzy změnil
8. HISTORIE REVIZÍ — přidej nový řádek s verzí, datem a co se změnilo

PRAVIDLA:
- NEPOVINUJ věty do budoucnosti — piš pouze to, co je zaznamenáno v systému.
- ZACHOVEJ strukturu YAML frontmatteru — aktualizuj datum_posledni_aktualizace, verzi a status_revize: ke_kontrole_clovekem.
- VŽDY uvedi: "Tento dokument je AI-generovaný — vyžaduje lidskou kontrolu."
- NEZMĚŇ stavy tvrzení nebo důkazů — pouze shrnuj.
- KDYŽ chybí informace, napiš „[ověřit]“ nebo „[doplnit]“ místo domněnky.
```
