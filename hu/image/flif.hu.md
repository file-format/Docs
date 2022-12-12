---
date: 2020-08-12
keywords: flif, .flif, flif fájlformátum, flif fájlok megnyitása, .flif kiterjesztése, flif kiterjesztése
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: FLIF fájlformátum
linktitle: FLIF
description: "Ismerje meg a FLIF fájlformátumot és az API-kat, amelyek FLIF fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Mi az a FLIF fájl? ##

A FLIF (Free Lossless Image Format) egy veszteségmentes képformátum, amely a .flif kiterjesztést használja a fájlokhoz. A FLIF azt állítja, hogy a tömörítési arány tekintetében felülmúlja a [PNG](/hu/image/png/), a veszteségmentes [WebP](/hu/image/webp/), a veszteségmentes BPG-t és a veszteségmentes JPEG 2000-et. A FLIF progresszív átlapolást használ, aminek köszönhetően a kép bármely részleges letöltése veszteséges kódolásként használható a teljes képhez.

## Rövid története ##

A FLIF-et 2015 szeptemberében jelentették be, az alfa verziót pedig 2015 októberében adták ki. 2016 szeptemberében adták ki a FLIF első stabil verzióját.

## FLIF Design ##

A FLIF a CABAC (kontextushoz alkalmazkodó bináris aritmetikai kódolás), a MANIAC (Meta-Adaptive Near-zero Integer Aithmetic Coding) egy változatát használja a tömörítéshez. A MANIAC egy entrópiakódoló algoritmus, amelyet Jon Sneyers és Pieter Wuille fejlesztett ki. A MANIAC-ban a kontextusok a döntési fák csomópontjai, amelyeket a kódolási időben dinamikusan tanulnak meg. Ez a kontextusmodellt képspecifikusabbá teszi, és jobb tömörítést eredményez. A FLIF a következő funkciókkal rendelkezik:

- Támogatja a veszteségmentes tömörítést
- Támogatja a veszteséges tömörítést kódoló előfeldolgozással
- Támogatja a szürkeárnyalatot, az RGB-t és az RGBA-t
- Támogatja a csatornánként 1-16 bites színmélységet
- Támogatja a váltottsoros és nem váltott soros fájlokat
- Támogatja a részben letöltött fájlok progresszív dekódolását
- Támogatja az animációkat
- Támogatja a beágyazott ICC színprofilokat, az Exif és XMP metaadatokat
- Korlátozottan támogatja a nyers kamerafájlok tömörítését (RGGB)

## FLIF fájlformátum ##

A FLIF fájl a következő négy részből áll:

## Fő fejléc ##

A fő fejléc tartalmazza a fő metaadatokat, beleértve a szélességet, magasságot, színmélységet és a keretek számát.

|Típus|Érték|Leírás|
|---|---|---|
|4 bájt|"FLIF"|Magic|
|4 bit|3 = ni még; 4 = i még; 5 = ni anim; 6 = i anim|Váltottsorolás, animáció|
|4 bit|1 = szürkeárnyalatos; 3 = RGB; 4 = RGBA|Csatornák száma (nb_channels)|
|1 bájt|'0','1','2' ('0'=egyéni)|Bájt csatornánként (Bpc)|
|varint|szélesség-1|Szélesség|
|varint|magasság-1|Magasság|
|varint|nb_frames-2 (csak animáció esetén)|Képek száma (nb_frames)|

## Metaadat-darabok ##

Ez a rész nem pixeles, például Exif/XMP metaadatokat, ICC színprofilt stb. tartalmaz, amelyek DEFLATE tömörítéssel vannak kódolva. Ezek a darabok a PNG-darabokhoz hasonlóan vannak definiálva, azzal a különbséggel, hogy a tokmány mérete változó számú bájttal van kódolva. A darabok neve 4 betűből (4 bájtból) vagy 32 alatti értékből állhat, ami nem kötelező darabot jelez.

A következő példa az opcionális tokmányokra:

|Részlet neve|Leírás|Tartalom (DEFLATE-dekompresszió után)|
|---|---|---|
|iCCP|ICC színprofil|nyers ICC színprofil adatok|
|eXif|Exif metadata|"Exif\0\0" fejléc, majd egy TIFF-fejléc és az EXIF-adatok|
|eXmp|XMP-metaadatok|Az XMP egy csak olvasható xpacketben található, kitöltés nélkül|

### Elnevezési ###

- **Első betű**: A nagybetűket a kritikus, a kisbetűket pedig a nem kritikus darabokhoz használják.
- **Második betű**: A nagybetűket a nyilvános, a kisbetűket pedig a privát darabokhoz használják
- **Harmadik betű**: A nagybetűk a kép helyes megjelenítéséhez szükséges tokmányokhoz használatosak, a kisbetűk pedig nem fontosak a kép megjelenítéséhez.
- **Negyedik betű**: A nagybetűket a vakon biztonságosan másolható tokmányokhoz használják. A kisbetűs tokmányok a képadatoktól függenek.

## Második fejléc ##

Ez tartalmazza a pixelek tényleges kódolására vonatkozó információkat.

|Típus|Leírás|Állapot|Alapértelmezett érték|
|---|---|---|---|
|1 bájt|NUL bájt (0x00), egy FLIF16 bitfolyam csonkneve||
|uni_int(1,16)|Csatorna bit/pixel|Bpc == '0': ismétlés(nb_channels)|8, ha Bpc == '1', 16, ha Bpc == '2'|
|uni_int(0,1)|Jelző: alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|Curkok száma|nb_frame > 1||
|uni_int(0,60_000)|Keretek késleltetése ms-ban|nb_frames > 1: ismétlés(nb_frames)|
|uni_int(0,1)|Jelző: has_custom_cutoff_and_alpha|||
|uni_int(1,128)|cutoff|has_custom_cutoff_and_alpha|2|
|uni_int(2,128)|alfa osztó|van_egyéni_vágás_és_alpha|19|
|uni_int(0,1)|Jelző: has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|van_egyedi_esélye||
|változó|Átalakítások (lásd lent)|||
|uni_int(1) = 0|Indikátor bit: transzformációkkal kész|||
|uni_int(0,2)|Láthatatlan képpont-előrejelző|alfa_nulla && váltott soros && az alfa tartomány nullát tartalmaz||

**Csatornák**

|Csatornaszám|Leírás|
|---|----|
|0|Piros vagy Szürke|
|1|Zöld|
|2|Kék|
|3|Alfa|

**Átváltozások**

|Típus|Leírás|
|---|---|
|uni_int(1) = 1|Indikátor bit: még nem készült el|
|uni_int(0,13)|Transformációs azonosító|
|változó|Transformációs adatok (transzformációtól függően)|

Az átalakítást a pixeladatok módosítására használják a jobb tömörítés érdekében, és nyomon követik a ténylegesen előforduló pixelértékeket.

## Pixel adatok ##

Ez a rész a tényleges pixeladatokat tartalmazza MANIAC entrópia kódolással kódolva. A pixelek kódolhatók váltottsoros vagy nem váltottsoros kódolással.

### Váltottsoros módszer ###

Ebben a módszerben a nagyítási szinteket határozzák meg. A 0-s nagyítási szint a teljes képhez, az 1-es nagyítási szint minden páros sorhoz, a 2-es nagyítási szint az 1-es nagyítási szint minden páros számú oszlopához használatos. Más szóval, minden páros számú 2k-s nagyítási szint a kép, 1:2^k méretarányban. A nagyítási szintek a legmagasabbtól a legalacsonyabbig vannak kódolva.

### Nem váltott soros módszer ###

Ennél a módszernél a MANIAC fák kódolása azonnal megkezdődik, majd a képpontok kódolása következik.

## Referenciák ##

- [FLIF - Wikipédia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

