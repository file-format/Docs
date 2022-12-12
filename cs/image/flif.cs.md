---
date: 2020-08-12
keywords: flif, .flif, formát souboru flif, jak otevřít soubory flif, přípona .flif, přípona flif
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formát souboru FLIF
linktitle: FLIF
description: "Přečtěte si o formátu souboru FLIF a rozhraních API, která mohou vytvářet a otevírat soubory FLIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Co je soubor FLIF? ##

FLIF (Free Lossless Image Format) je bezztrátový formát obrázků, který pro své soubory používá příponu .flif. FLIF tvrdí, že překonává [PNG](/cs/image/png/), bezztrátové [WebP](/cs/image/webp/), bezztrátové BPG a bezztrátové JPEG 2000 z hlediska kompresního poměru. FLIF používá progresivní prokládání, díky kterému lze jakékoli částečné stažení obrázku použít jako ztrátové kódování pro celý obrázek.

## Stručná historie ##

FLIF byl oznámen v září 2015 a alfa verze byla vydána v říjnu 2015. V září 2016 byla vydána první stabilní verze FLIF.

## Design FLIF ##

FLIF používá pro kompresi variantu CABAC (Kontextově adaptivní binární aritmetické kódování), MANIAC (Meta-Adaptivní Near-zero Integer Arithmetic Coding). MANIAC je entropický kódovací algoritmus vyvinutý Jonem Sneyersem a Pieterem Wuillem. V MANIAC jsou kontexty uzly rozhodovacích stromů, které se dynamicky učí v době kódování. Díky tomu je kontextový model více specifický pro obrázky a výsledkem je lepší komprese. FLIF má následující vlastnosti:

- Podporuje bezeztrátovou kompresi
- Podporuje ztrátovou kompresi s předzpracováním kodéru
- Podporuje stupně šedi, RGB a RGBA
- Podporuje barevnou hloubku 1 až 16 bitů na kanál
- Podporuje prokládané a neprokládané soubory
- Podporuje progresivní dekódování částečně stažených souborů
- Podporuje animace
- Podporuje vložené profily barev ICC, metadata Exif a XMP
- Má omezenou podporu pro kompresi souborů camera raw (RGGB)

## Formát souboru FLIF ##

Soubor FLIF má následující čtyři části:

## Hlavní záhlaví ##

Hlavní záhlaví obsahuje hlavní metadata včetně šířky, výšky, barevné hloubky, počtu snímků.

|Typ|Hodnota|Popis|
|---|---|---|
|4 bajty|"FLIF"|Kouzlo|
|4 bity|3 = ni stále; 4 = i stále; 5 = ni anim; 6 = i anim|Prokládání, animace|
|4 bity|1 = stupně šedi; 3 = RGB; 4 = RGBA|Počet kanálů (nb_channels)|
|1 bajt|'0','1','2' ('0'=vlastní)|Bajty na kanál (Bpc)|
|varint|šířka-1|šířka|
|varint|výška-1|Výška|
|varint|nb_frames-2 (pouze v případě animace)|Počet snímků (nb_frames)|

## Části metadat ##

Tato část obsahuje nepixelová metadata, jako jsou Exif/XMP metadata, barevný profil ICC atd., která jsou kódována pomocí komprese DEFLATE. Tyto bloky jsou definovány podobně jako bloky PNG s tím rozdílem, že velikost sklíčidla je kódována proměnným počtem bajtů. Názvy bloků mohou mít 4 písmena (4 bajty) nebo hodnotu nižší než 32 označující nepovinný blok.

Následuje příklad volitelných sklíčidel:

|Název bloku|Popis|Obsah (po dekompresi DEFLATE)|
|---|---|---|
|iCCP|profil barev ICC|surová data barevného profilu ICC|
|eXif|Exif metadata|"Exif\0\0" hlavička následovaná hlavičkou TIFF a EXIF data|
|eXmp|XMP metadata|XMP obsažená v xpacketu pouze pro čtení bez odsazení|

### Konvence pojmenování ###

- **První písmeno**: Velká písmena se používají pro kritické a malá písmena pro nekritické části.
- **Druhé písmeno**: Velká písmena se používají pro veřejné a malá písmena pro soukromé části
- **Třetí písmeno**: Velká písmena se používají pro sklíčidla, která jsou potřebná pro správné zobrazení obrázku a malá písmena nejsou pro zobrazení obrázku důležitá.
- **Čtvrté písmeno**: Velká písmena se používají pro sklíčidla, která lze bezpečně kopírovat naslepo. Sklíčidla s malými písmeny závisí na obrazových datech.

## Druhé záhlaví ##

To obsahuje informace týkající se skutečného kódování pixelů.

|Typ|Popis|Podmínka|Výchozí hodnota|
|---|---|---|---|
|1 byte|bajt NUL (0x00), název bloku bitového toku FLIF16||
|uni_int(1,16)|Bity na pixel kanálů|Bpc == '0': repeat(nb_channels)|8, pokud Bpc == '1', 16, pokud Bpc == '2'|
|uni_int(0,1)|Příznak: alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|Počet smyček|nb_frames > 1||
|uni_int(0,60_000)|Zpoždění snímků v ms|nb_frames > 1: repeat(nb_frames)|
|uni_int(0,1)|Příznak: has_custom_cutoff_and_alpha|||
|uni_int(1,128)|cutoff|has_custom_cutoff_and_alpha|2|
|uni_int(2,128)|dělitel alfa|has_custom_cutoff_and_alpha|19|
|uni_int(0,1)|Příznak: has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|has_custom_bitchance||
|proměnná|Transformace (viz níže)|||
|uni_int(1) = 0|Indikační bit: hotovo s transformacemi|||
|uni_int(0,2)|Prediktor neviditelných pixelů|alpha_zero && prokládaný && rozsah alfa zahrnuje nulu||

**Kanály**

|Číslo kanálu|Popis|
|---|----|
|0|Červená nebo šedá|
|1|Zelená|
|2|Modrá|
|3|Alfa|

**Proměny**

|Typ|Popis|
|---|---|
|uni_int(1) = 1|Indikační bit: ještě není hotovo|
|uni_int(0,13)|Identifikátor transformace|
|proměnná|Data transformace (závisí na transformaci)|

Transformace se používá k úpravě dat pixelů pro lepší kompresi a ke sledování skutečně se vyskytujících hodnot pixelů.

## Pixelová data ##

Tato část obsahuje aktuální pixelová data zakódovaná pomocí kódování entropie MANIAC. Pixely mohou být kódovány pomocí prokládaného nebo neprokládaného kódování.

### Prokládaná metoda ###

V této metodě jsou definovány úrovně přiblížení. Úroveň přiblížení 0 se používá pro celý obrázek, úroveň přiblížení 1 se používá pro všechny sudé řádky, úroveň přiblížení 2 se používá pro všechny sloupce úrovně přiblížení 1. Jinými slovy, každá úroveň přiblížení se sudým číslem 2k je převzorkovaná verze obrázek v měřítku 1:2^k. Úrovně přiblížení jsou kódovány od nejvyšší po nejnižší.

### Neprokládaná metoda ###

V této metodě začíná kódování stromů MANIAC bezprostředně následované kódováním pixelů.

## Reference ##

- [FLIF - Wikipedia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

