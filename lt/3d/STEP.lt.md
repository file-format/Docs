---
date: 2019-10-11
keywords: step, .step, step file format, how to open step files, .step extension, step extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: STEP failo formaat
linktitle: STEP
description: Luždirbti apie STEP failo formatą ir API, kurios gali sukurti ir atidaryti STEP failąs.
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## Kas yra STEP failas?

STEP failas yra plačiai naudojamas kompiuterinio projektavimo (CAD) duomenų mainų formatas. ISO komitetas jį standartizavo 1994 m. pavadinimu ISO 10303-21. ISO 10303-21 apibrėžia kodavimo mechanizmą, skirtą duomenims pateikti EXPRESS duomenų modeliavimo kalba. STEP failas taip pat žinomas kaip p21-File ir STEP Physical File. STEP faile naudojami failų plėtiniai yra .stp ir .step.

## Pagrindinė istorija

In 1994, the original Part 21 specification was issued. It has some bugs which were corrected by the technical corrigendum issued in 1996. Antrasis leidimas buvo paskelbtas 2002 m., kuriame buvo kelių duomenų skyrių klaidų ištaisymas ir plėtiniai. Trečiasis leidimas buvo paskelbtas 2016 m., kuriame buvo pridėtos prierašo ir nuorodų dalys, leidžiančios objektus ir reikšmes saugoti išoriniuose failuose. Buvo pridėtas UTF-8 palaikymas. Skaitmeniniai parašai buvo pridėti siekiant patikrinti failo turinį ir patvirtinti kredencialus. Taip pat buvo pridėta mainų struktūros suspaudimo ir saugojimo naudojant ZIP palaikymas.

## STEP failo formatas

The plain text format for a STEP-file consists of a sequence of records. The character set is defined as code points of ISO 10646. ISO-10303-21; yra pirmieji pirmojo įrašo simboliai. Komentarai yra apsupti /* ir */ simboliais. Paskutiniame įraše yra END-ISO-10303-21; jei STEP failas atitinka 2002 m. versiją. Jei jis atitinka 2016 m. versiją, po END-ISO-10303-21; gali būti vienas ar daugiau skaitmeninių parašų. terminatorius. Eilučių lūžiai žymimi \N\, o puslapių lūžiai – \F\.

STEP failas yra padalintas į skyrius, o jų pavadinimai yra rezervuoti terminai. Visos skiltys baigiasi ENDSEC įrašu ir turi būti toliau nurodyta tvarka.

- **ANTRAŠTĖ**: tai privaloma ir nepakartojama skiltis. Jį sudaro šie subjektai:
  - file_description (mandatory)
  - "failo_pavadinimas (privalomas)"
  - "file_schema (privaloma)"
  - "schema_population (neprivaloma)"
  - "file_population (neprivaloma)"
  - "sekcijos_kalba (neprivaloma)"
  - "section_context (neprivaloma)"
- **ANCHOR**: tai pasirenkama nesikartojanti dalis, kuri buvo pristatyta 2016 m. versijoje. Jis apibrėžia išorinius egzempliorių pavadinimus, kad būtų galima juos nurodyti.
- **NUORODOS**: tai pasirenkama nesikartojanti skiltis, kuri taip pat buvo pristatyta 2016 m. versijoje. Kiekvienas šio skyriaus įrašas susieja įrašo / vertės egzemplioriaus pavadinimą su egzemplioriumi / reikšme išoriniame faile.
- **DUOMENYS**: tai pasirenkama kartojama sekcija, kurioje yra pagrindinis modelio egzemplioriaus turinys.
- **SIGNATURE**: It is an optional repeatable section that was introduced in the 2016 version. It holds the digital signature to verify the file's content or to validate credentials.

## Nuorodos

- [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)

