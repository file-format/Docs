---
date: 2020-08-12
keywords: flif, .flif, flif file format, how to open flif files, .flif extension, flif extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: FLIF failo formaat
linktitle: FLIF
description: Luždirbti apie FLIF failo formatą ir API, kurios gali sukurti ir atidaryti FLIF failąs.
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Kas yra FLIF failas? ##

FLIF (Free Lossless Image Format) yra be nuostolių vaizdo formatas, kurio failams naudojamas .flif plėtinys. FLIF teigia, kad glaudinimo laipsniu lenkia [PNG](/image/png/), be nuostolių [WebP](/image/webp/), be nuostolių BPG ir be nuostolių JPEG 2000. FLIF naudoja progresyvų persipynimą, dėl kurio bet koks dalinis vaizdo atsisiuntimas gali būti naudojamas kaip viso vaizdo nuostolingas kodavimas.

## Trumpa istorija ##

FLIF was announced in September 2015, and the alpha version was released in October 2015. 2016 m. rugsėjį buvo išleista pirmoji stabili FLIF versija.

## FLIF dizainas ##

FLIF glaudinimui naudoja CABAC (konteksto adaptyvaus dvejetainio aritmetinio kodavimo), MANIAC (meta-adaptive Near-zero Integer Aithmetic Coding) variantą. MANIAC yra entropijos kodavimo algoritmas, kurį sukūrė Jon Sneyers ir Pieter Wuille. MANIAC kontekstai yra sprendimų medžių mazgai, kurie išmokstami dinamiškai koduojant. Dėl to kontekstinis modelis labiau būdingas vaizdams ir geresnis suspaudimas. FLIF turi šias funkcijas:

- Palaiko be nuostolių suspaudimą
- Palaiko nuostolingą glaudinimą naudojant kodavimo įrenginio išankstinį apdorojimą
- Palaiko pilkų tonų, RGB ir RGBA
- Palaiko spalvų gylį nuo 1 iki 16 bitų viename kanale
- Palaiko susipynusius ir nepintus failus
- Palaiko laipsnišką iš dalies atsisiųstų failų dekodavimą
- Palaiko animacijas
- Palaiko įterptus ICC spalvų profilius, Exif ir XMP metaduomenis
- Turi ribotą fotoaparato neapdorotų failų (RGGB) glaudinimo palaikymą

## FLIF failo formatas ##

FLIF failą sudaro šios keturios dalys:

## Pagrindinė antraštė ##

Pagrindinėje antraštėje yra pagrindiniai metaduomenys, įskaitant plotį, aukštį, spalvų gylį, kadrų skaičių.

|Tipas|Vertė|Aprašymas|
|---|---|---|
|4 baitai|FLIF|Magic|
|4 bitai|3 = ni vis dar; 4 = aš vis dar; 5 = ni anim; 6 = i anim|Interlacing, animation|
|4 bitai|1 = pilkos spalvos tonai; 3 = RGB; 4 = RGBA|Kanalų skaičius (nb_channels)|
|1 baitas|'0','1','2' ('0'=priskirtas)|Baitai kanale (Bpc)|
|varint|plotis-1|Plotis|
|varint|aukštis-1|Aukštis|
|varint|nb_frames-2 (tik jei animacija)|Kadrų skaičius (nb_frames)|

## Metaduomenų dalys ##

Šioje dalyje yra ne pikselių, tokių kaip Exif/XMP metaduomenys, ICC spalvų profilis ir kt., kurie užkoduoti naudojant DEFLATE glaudinimą. Šie gabalai apibrėžiami panašiai kaip PNG gabalai, tačiau skirtumas yra tas, kad griebtuvo dydis yra užkoduotas kintamu baitų skaičiumi. Dalių pavadinimai gali būti sudaryti iš 4 raidžių (4 baitai) arba mažesnė nei 32 reikšmė, nurodanti neprivalomą gabalą.

Toliau pateikiamas pasirenkamų griebtuvų pavyzdys:

|Laiko pavadinimas|Aprašymas|Turinys (po DEFLATE-dekompresijos)|
|---|---|---|
|iCCP|ICC spalvų profilis|neapdoroti ICC spalvų profilio duomenys|
|eXif|Exif metaduomenys|Exif\0\0 antraštė, po kurios yra TIFF antraštė ir EXIF duomenys|
|eXmp|XMP metaduomenys|XMP yra tik skaitomame xpacket be užpildymo|

### Įvardijimo konvencija ###

- **Pirmoji raidė**: didžiosios raidės naudojamos kritinėms raidėms, o mažosios - nekritinėms dalims.
- **Antra raidė**: didžiosios raidės naudojamos viešai, o mažosios - privačioms raidėms
- **Trečia raidė**: didžiosios raidės naudojamos griebtuvams, kurių reikia, kad vaizdas būtų rodomas teisingai, o mažosios raidės nėra svarbios, kad vaizdas būtų rodomas.
- **Ketvirtoji raidė**: didžiosios raidės naudojamos griebtuvams, kuriuos galima saugiai kopijuoti aklai. Mažųjų raidžių griebtuvai priklauso nuo vaizdo duomenų.

## Antroji antraštė ##

Čia pateikiama informacija apie tikrąjį pikselių kodavimą.

|Tipas|Aprašymas|Būklė|Numatytoji reikšmė|
|---|---|---|---|
|1 baitas|NUL baitas (0x00), FLIF16 bitų srauto gabalo pavadinimas||
|uni_int(1,16)|Kanalų bitai pikselyje|Bpc == '0': pakartokite(nb_channels)|8, jei Bpc == '1', 16, jei Bpc == '2'|
|uni_int(0,1)|Žyma: alfa_nulis|nb_channels > 3|0|
|uni_int(0,100)|Kilpų skaičius|nb_frames > 1||
|uni_int(0,60_000)|Kadro delsa ms|nb_frames > 1: pakartokite(nb_frames)|
|uni_int(0,1)|Žyma: turi_custom_cutoff_and_alpha|||
|uni_int(1,128)|riba|turi_priskirtą_ribą_ir_alpha|2|
|uni_int(2,128)|alfa daliklis|turi_priskirtą_ribą_ir_alpha|19|
|uni_int(0,1)|Žyma: turi_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|turi_priskirtą_susitikimą||
|kintamasis|Transformacijos (žr. toliau)|||
|uni_int(1) = 0|Indikatoriaus bitas: atliktas su transformacijomis|||
|uni_int(0,2)|Nematomo pikselio numatymo priemonė|alfa_nulis && persipynęs && alfa diapazonas apima nulį||

**Kanalai**

|Kanalo numeris|Aprašymas|
|---|----|
|0|Raudona arba Pilka|
|1|Žalias|
|2|Mėlyna|
|3|Alfa|

**Transformacijos**

|Tipas|Aprašymas|
|---|---|
|uni_int(1) = 1|Indikatoriaus bitas: dar nepadaryta|
|uni_int(0,13)|Transformacijos identifikatorius|
|kintamasis|Transformacijos duomenys (priklauso nuo transformacijos)|

Transformacija naudojama pikselių duomenims modifikuoti, kad būtų geresnis suspaudimas, ir sekti faktiškai atsirandančias pikselių reikšmes.

## Pikselių duomenys Nr.

Šioje dalyje yra tikrieji pikselių duomenys, užkoduoti naudojant MANIAC entropijos kodavimą. Pikseliai gali būti užkoduoti naudojant persipynusią arba neinterlaced kodavimą.

### Sujungimo metodas ###

In this method, zoomlevels are defined. Zoomlevel 0 is used for the full image, zoomlevel 1 is used for all even-numbered rows, zoomlevel 2 is used for all even-numbered columns of zoomlevel 1. Kitaip tariant, kiekvienas lyginis 2k mastelio keitimo lygis yra sumažinta vaizdo versija, kurios mastelis yra 1:2^k. Mastelio keitimo lygiai yra užkoduoti nuo aukščiausio iki žemiausio.

### Neišsipynęs metodas ###

Taikant šį metodą, MANIAC medžių kodavimas prasideda iš karto, o po to - pikselių kodavimas.

## Nuorodos Nr.

- [FLIF - Wikipedia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

