---
date: 2019-12-13
keywords: flac, flac fájlformátum, .flac kiterjesztése, flac fájl, flac vs mp3
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Ismerje meg a FLAC fájlformátumot és az API-kat, amelyek FLAC fájlokat hozhatnak létre és nyithatnak meg."
title: FLAC fájlformátum
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## Mi az a FLAC fájl?

A FLAC (Free Lossless Audio Codec) egy veszteségmentes tömörítésű hangkódolási formátum, amelyet a Xiph.Org Foundation fejlesztett ki. A FLAC egy jogdíjmentes nyílt formátum, amelyet a .flac kiterjesztéssel mentünk. A FLAC algoritmussal tömörített digitális hang mérete általában 50-70 százalékra csökken. A FLAC fájlok kicsomagolhatók az eredeti hangfájlok azonos másolatává.

## FLAC fájl formátum

Ez a FLAC bitfolyam áttekintése.

- **fLaC marker**: Ez a jelző a stream elejéhez kerül hozzáadásra. Ezt egy vagy több metaadatblokk követi.
- **Metaadatblokkok**: 128 féle metaadatblokkot támogat a FLAC; jelenleg a következők vannak meghatározva.
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **KERET**: Az audioadatok egy vagy több hangkockából állnak.
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## A FLAC fájlformátum rövid története

Josh Coalson 2000-ben kezdte meg a FLAC fejlesztését. A FLAC első verzióját 2001. július 20-án adták ki. A FLAC-ot 2003. január 20-án a Xiph.Org zászló alá vették. A FLAC fejlesztése átkerült a Xiph.Org git adattárba az 1.3.0 verzió megjelenése 2013. március 26-án.

## A FLAC projekt összetétele

A FLAC projekt a következőkből áll:

- Stream formátumok.
- Egyszerű konténerformátum az adatfolyamhoz (FLAC).
- libFLAC: Referenciakódolók, dekódolók és metaadat-interfészek könyvtára.
- libFLAC++: A libFLAC objektumorientált burkolója.
- flac: Parancssori program a FLAC adatfolyamok kódolására és dekódolására.
- metaflac: A FLAC parancssori metaadat-szerkesztője.
- Bemeneti bővítmények zenelejátszókhoz, például Winamp, XMMX stb.
- Ogg konténer formátum (Ogg FLAC).

## FLAC tervezés

A zene sűrűségétől és amplitúdójától függően a tömörített fájl mérete 80%-kal kisebb lehet, mint az eredeti fájlé.

### Forráskódoló ###

- Csak egész számmintákat támogat, lebegőpontos mérést nem. Mintánként 4 és 32 bit közötti PCM bitfelbontást és 1 Hz és 65 535 Hz közötti mintavételi frekvenciát képes kezelni. A FLAC kódolás mintánként 24 bitre korlátozódik.
- A csatornák csoportosíthatók, hogy kihasználják a csatornaközi összefüggéseket a tömörítés növelése érdekében.
- A CRC ellenőrző összegeket a sérült keretek azonosítására használják.
- A hangminták konvertálásához a FLAC lineáris előrejelzést használ.

### Metaadatok ###

- A FLAC támogatja a ReplayGaint (a hang hangerejének érzékelésére és normalizálására).
- A FLAC ugyanazt a rendszert használja, mint a Vorbis megjegyzéseiben a címkézéshez.
- A libFLAC-ot a legtöbb FLAC-alkalmazás használja kódolásra/dekódolásra.
- A libFLAC API folyamokba, kereshető adatfolyamokba és fájlokba van szervezve, hogy növelje az absztrakciót az alap FLAC bitfolyamtól.

### Tömörítés ###

A libFLAC 0 és 8 közötti tömörítési szintet használ, ahol a 0 a leggyorsabb, a 8 pedig a leglassabb tömörítési szint. A tömörített fájlok mindig veszteségmentesek, bár a kompromisszum a sebesség és a méret között van.

## FLAC vs MP3
Az MP3 veszteséges tömörítési formátum, ami azt jelenti, hogy a tömörítés alkalmazása után levághatja a hang egy részét, hogy csökkentse a méretét. Míg a FLAC veszteségmentes fájlformátum, ami azt jelenti, hogy a hangot a legtisztább formában hallhatja. Korábban a veszteségmentes fájlformátumok CDA vagy WAV voltak, amelyek nem voltak olyan helytakarékosak, mint a FLAC. Az alábbi táblázat a két formátum összehasonlítását mutatja be néhány fontos kifejezés esetében:

|Termin|FLAC|MP3|
---|---|---|
|**Adatminőség**|Nincs hang adatvesztés| Egyes adatok elveszhetnek az audio adatok tömörítésekor|
|**Méret**|Nagyobb fájlméret a veszteséges formátumokhoz képest. Tehát nagyobb tárolókapacitás kell| Kisebb fájlméret, alkalmas kis tárhellyel rendelkező kompakt audioeszközökön való lejátszásra |
|**Hardverkövetelmények**| Kiváló minőségű audiofelszerelésre és hatalmas tárolókapacitásra van szüksége | Hatalmas audiokönyvtárak menthetők el kisebb tárhelyen. Alkalmas kézi eszközökhöz, például audiolejátszókhoz vagy mobiltelefonokhoz|
|**Terjesztés az interneten**|Nem könnyen terjeszthető az interneten a hatalmas fájlméret miatt |A kompakt fájlméret megkönnyíti az interneten történő terjesztést|
|**Kompatibilitás**|A legnépszerűbb zene- és hanghallgatási kodek, amely nagyjából kompatibilis a bolygó minden eszközével. Kompatibilis új generációs PC-kkel, telefonokkal, AV-vevőkkel, Blu-ray lejátszókkal, streaming eszközökkel, például Roku vagy Fire TV|

## Referenciák ##

- [FLAC - Wikipédia](https://en.wikipedia.org/wiki/FLAC)

