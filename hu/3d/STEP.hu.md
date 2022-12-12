---
date: 2019-10-11
keywords: step, .step, step fájlformátum, lépésfájlok megnyitása, .step kiterjesztése, lépés kiterjesztése
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: STEP fájlformátum
linktitle: STEP
description: "Ismerje meg a STEP fájlformátumot és az API-kat, amelyek STEP fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## Mi az a STEP fájl?

A STEP fájl egy széles körben használt adatcsere-formátum a számítógépes tervezéshez (CAD). Az ISO bizottság 1994-ben szabványosította "ISO 10303-21" néven. Az ISO 10303-21 meghatározza az adatok EXPRESS adatmodellező nyelven történő megjelenítésének kódolási mechanizmusát. A STEP-fájl más néven p21-File és STEP Physical File. A STEP fájlokhoz használt kiterjesztések a .stp és a .step.

## Alaptörténelem

1994-ben adták ki az eredeti, Part 21 specifikációt. Vannak benne hibák, amelyeket az 1996-ban kiadott technikai helyesbítés javított ki. A második kiadás 2002-ben jelent meg, amely tartalmazta a helyesbítést és több adatrész kiterjesztését. A harmadik kiadás 2016-ban jelent meg, amely horgony- és hivatkozási részekkel egészítette ki, amelyek lehetővé tették az entitások és értékek külső fájlokban való tárolását. UTF-8 támogatás hozzáadva a karakterláncokhoz. Digitális aláírások kerültek hozzáadásra a fájl tartalmának ellenőrzésére és a hitelesítő adatok érvényesítésére. A cserestruktúra ZIP használatával történő tömörítésének és tárolásának támogatása is hozzáadásra került.

## STEP fájlformátum

A STEP-fájl egyszerű szöveges formátuma rekordok sorozatából áll. A karakterkészlet az ISO 10646 kódpontjaiként van meghatározva. "ISO-10303-21;" ezek az első karakterek az első rekordban. A megjegyzéseket „/*” és „*/” karakter veszi körül. Az utolsó rekord a következőt tartalmazza: "END-ISO-10303-21;" ha a STEP-fájl megfelel a 2002-es verziónak. Abban az esetben, ha megfelel a 2016-os verziónak, egy vagy több digitális aláírás lehet az „END-ISO-10303-21;” után. Végrehajtó. A sortöréseket "\N\", az oldaltöréseket pedig "\F\" jelöli.

A STEP fájl szakaszokra van felosztva, és a nevük fenntartott kifejezések. Minden szakasz az "ENDSEC" rekorddal végződik, és az alábbi sorrendben kell szerepelnie.

- **HEADER**: Ez egy kötelező és nem megismételhető szakasz. A következő entitásokból áll:
  - file_description (mandatory)
  - file_name (mandatory)
  - file_schema (mandatory)
  - schema_population (optional)
  - file_population (optional)
  - section_language (optional)
  - section_context (optional)
- **ANCHOR**: Ez egy opcionális, nem ismétlődő szakasz, amelyet a 2016-os verzióban vezettek be. Meghatározza a példányok külső neveit, hogy hivatkozni lehessen rájuk.
- **REFERENCIA**: Ez egy opcionális, nem ismétlődő szakasz, amelyet a 2016-os verzióban is bevezettek. Ebben a szakaszban minden bejegyzés egy bejegyzés/érték példánynevet társít egy külső fájlban lévő példányhoz/értékhez.
- **ADATOK**: Ez egy opcionális megismételhető szakasz, amely tartalmazza a modellpéldány alapvető tartalmát.
- **ALÁÍRÁS**: Ez egy opcionális megismételhető szakasz, amelyet a 2016-os verzióban vezettek be. Ez tartalmazza a digitális aláírást a fájl tartalmának vagy a hitelesítő adatok érvényesítéséhez.

## Hivatkozások

- [ISO 10303-21 - Wikipédia](https://en.wikipedia.org/wiki/ISO_10303-21)

