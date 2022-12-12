---
date: 2019-10-11
keywords: step, .step, formát souboru step, jak otevřít soubory step, přípona .step, přípona kroku
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formát souboru STEP
linktitle: STEP
description: "Přečtěte si o formátu souborů STEP a rozhraních API, která mohou vytvářet a otevírat soubory STEP."
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## Co je soubor STEP?

Soubor STEP je široce používaný formát pro výměnu dat pro počítačově podporované navrhování (CAD). Byla standardizována v roce 1994 komisí ISO pod názvem „ISO 10303-21“. ISO 10303-21 definuje kódovací mechanismus pro reprezentaci dat v jazyce EXPRESS pro modelování dat. Soubor STEP je také známý jako soubor p21 a fyzický soubor STEP. Přípony souborů používané pro soubor STEP jsou .stp a .step.

## Základní historie

V roce 1994 byla vydána původní specifikace části 21. Obsahuje některé chyby, které byly opraveny technickou opravou vydanou v roce 1996. Druhé vydání bylo zveřejněno v roce 2002, které zahrnovalo opravu a rozšíření pro několik oddílů údajů. Třetí vydání bylo publikováno v roce 2016, které přidalo kotevní a referenční sekce, které umožňovaly ukládání entit a hodnot do externích souborů. Podpora UTF-8 byla přidána z řetězců. Byly přidány digitální podpisy pro ověření obsahu souboru a ověření přihlašovacích údajů. Byla také přidána podpora pro kompresi a ukládání struktury výměny pomocí ZIP.

## Formát souboru STEP

Formát prostého textu pro soubor STEP se skládá ze sekvence záznamů. Znaková sada je definována jako kódové body normy ISO 10646. "ISO-10303-21;" jsou první znaky v prvním záznamu. Komentáře jsou obklopeny znaky "/*" a "*/". Poslední záznam obsahuje "END-ISO-10303-21;" pokud je soubor STEP v souladu s verzí z roku 2002. V případě, že odpovídá verzi z roku 2016, může být za „END-ISO-10303-21;“ jeden nebo více digitálních podpisů; terminátor. Konce řádků jsou označeny "\N\" a konce stránek jsou označeny "\F\".

Soubor STEP je rozdělen do sekcí a jejich názvy jsou vyhrazené termíny. Všechny sekce končí záznamem „ENDSEC“ a musí být v níže uvedeném pořadí.

- **HEADER**: Toto je povinná a neopakovatelná část. Skládá se z následujících subjektů:
  - file_description (mandatory)
  - file_name (mandatory)
  - file_schema (mandatory)
  - schema_population (optional)
  - file_population (optional)
  - section_language (optional)
  - section_context (optional)
- **ANCHOR**: Jedná se o volitelnou neopakující se sekci, která byla představena ve verzi 2016. Definuje externí názvy pro instance, aby na ně bylo možné odkazovat.
- **REFERENCE**: Jedná se o volitelnou neopakující se sekci, která byla také představena ve verzi 2016. Každá položka v této části přidružuje název instance položky/hodnoty k instanci/hodnotě v externím souboru.
- **DATA**: Jedná se o volitelnou opakovatelnou sekci, která obsahuje základní obsah instance modelu.
- **SIGNATURE**: Jedná se o volitelnou opakovatelnou sekci, která byla zavedena ve verzi 2016. Obsahuje digitální podpis pro ověření obsahu souboru nebo ověření přihlašovacích údajů.

## Reference

- [ISO 10303-21 - Wikipedie](https://en.wikipedia.org/wiki/ISO_10303-21)

