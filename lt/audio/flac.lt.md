---
date: 2019-12-13
keywords: flac, flac file format, .flac extension, flac file, flac vs mp3
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Luždirbti apie FLAC failo formatą ir API, kurios gali sukurti ir atidaryti FLAC failąs.
title: FLAC failo formaat
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## Kas yra FLAC failas?

FLAC (Free Lossless Audio Codec) yra be nuostolių suspaudimo garso kodavimo formatas, kurį sukūrė Xiph.Org Foundation. FLAC yra nemokamas atviras formatas, kuris išsaugomas su plėtiniu .flac. Skaitmeninis garsas, suspaustas naudojant FLAC algoritmą, paprastai sumažinamas iki 50–70 procentų. FLAC failus galima išspausti iki identiškos originalių garso failų kopijos.

## FLAC failo formatas

Tai yra FLAC bitų srauto apžvalga.

- **fLaC žymeklis**: šis žymeklis pridedamas prie srauto pradžios. Po jo seka vienas ar keli metaduomenų blokai.
- **Metaduomenų blokai**: FLAC palaiko 128 rūšių metaduomenų blokus; šiuo metu apibrėžiami šie dalykai.
  - "**STREAMINFO**: yra informacijos apie visą srautą."
  - "**TAIKOMA**: ją naudoja trečiųjų šalių programos identifikavimui."
  - "**PADDING**: naudojamas rezervuoti vietą metaduomenims, jei metaduomenys bus redaguojami po užkodavimo. Kai metaduomenys redaguojami, užpildymas pakeičiamas tikrais metaduomenimis."
  - "**PAIEŠKOS LENTELĖ**: pasirenkama lentelė paieškos taškams saugoti."
  - "**VORBIS_COMMENT**: naudojamas žmogaus skaitomoms raktų/reikšmių poroms saugoti."
  - "**CUESHEET**: naudojamas informacinio lapo informacijai saugoti."
  - "**PICTURE**: naudojamas nuotraukoms saugoti."
- **FRAME**: garso duomenis sudaro vienas ar daugiau garso kadrų.
  - "**FRAME_HEADER**: yra pagrindinė informacija apie srautą."
  - "**PAKADRAS**: siekiant sumažinti sudėtingumą, atskiri antriniai kadrai yra koduojami atskirai kadre (po vieną kadrą kanale)."
  - "**FRAME_FOOTER**: yra viso kadro CRC."

## Trumpa FLAC failo formato istorija

Josh Coalson began the development of FLAC in 2000. Pirmoji FLAC versija buvo išleista 2001 m. liepos 20 d. FLAC buvo įtrauktas į Xiph.Org vėliavą 2003 m. sausio 20 d. FLAC kūrimas buvo perkeltas į Xiph.Org git saugyklą, kovo 26 d. išleidus 1.3.0 versiją 2013 m.

## FLAC projekto sudėtis

FLAC projektą sudaro:

- Srautinio formatai.
- Paprastas srauto konteinerio formatas (FLAC).
- libFLAC: nuorodų koduotuvų, dekoderių ir metaduomenų sąsajos biblioteka.
- libFLAC++: į objektą orientuotas libFLAC paketas.
- flac: komandinės eilutės programa, skirta koduoti ir iššifruoti FLAC srautus.
- metaflac: komandų eilutės metaduomenų rengyklė, skirta FLAC.
- Įvesties papildiniai muzikos grotuvams, tokiems kaip Winamp, XMMX ir kt.
- Ogg konteinerio formatas (Ogg FLAC).

## FLAC dizainas

Priklausomai nuo muzikos tankio ir amplitudės, suspausto failo dydis gali būti 80 % mažesnis nei pradinio failo.

### Šaltinio kodavimo priemonė ###

- Jis palaiko tik sveikųjų skaičių pavyzdžius, o ne slankiojo kablelio. Jis gali apdoroti PCM bitų skiriamąją gebą nuo 4 iki 32 bitų vienam mėginiui ir atrankos dažnį nuo 1 Hz iki 65 535 Hz. FLAC kodavimas yra apribotas iki 24 bitų vienam pavyzdžiui.
- Kanalai gali būti sugrupuoti, kad būtų galima pasinaudoti tarpkanalių koreliacijomis ir padidinti glaudinimą.
- CRC kontrolinės sumos naudojamos pažeistiems kadrams nustatyti.
- Garso pavyzdžiams konvertuoti FLAC naudoja linijinį numatymą.

### Metaduomenys ###

- FLAC palaiko ReplayGain (naudojamas garso garsumui suvokti ir normalizuoti).
– FLAC žymėjimui naudoja tą pačią sistemą, kuri naudojama Vorbis komentaruose.
- libFLAC kodavimui / dekodavimui naudoja dauguma FLAC programų.
- libFLAC API suskirstyta į srautus, ieškomus srautus ir failus, siekiant padidinti abstrakciją nuo bazinio FLAC bitų srauto.

### Suspaudimas ###

libFLAC naudoja suspaudimo lygius nuo 0 iki 8, kur 0 yra greičiausias, o 8 yra lėčiausias glaudinimo lygis. Suspausti failai visada yra be nuostolių, nors kompromisas yra tarp greičio ir dydžio.

## FLAC prieš MP3
MP3 yra nuostolingas glaudinimo formatas, tai reiškia, kad pritaikius glaudinimą jis gali iškirpti tam tikrą garso dalį, kad sumažintų jo dydį. Tuo tarpu FLAC yra neprarandantis failo formatas, o tai reiškia, kad galite girdėti garsą gryniausia forma. Anksčiau be nuostolių failų formatai buvo CDA arba WAV, kurie nebuvo daug vietos taupantys kaip FLAC. Šioje lentelėje bus parodytas šių dviejų formatų palyginimas pagal kai kuriuos svarbius terminus:

|Terminas|FLAC|MP3|
---|---|---|
|**Duomenų kokybė**|Neprarandami garso duomenys| Kai kurie duomenys gali būti prarasti glaudinant garso duomenis|
|**Dydis**|Didesnis failo dydis, palyginti su nuostolingais formatais. Taigi reikia didesnės atminties talpos| Mažesnis failo dydis, tinkamas leisti kompaktiškuose garso įrenginiuose, kuriuose yra mažai vietos saugykloje |
|**Aparatinės įrangos reikalavimai**| Reikia aukštos kokybės garso įrangos ir didžiulės atminties talpos | Didelės garso bibliotekos gali būti išsaugotos mažesnėje saugyklos vietoje. Tinka nešiojamiems įrenginiams, tokiems kaip garso grotuvai ar mobilieji telefonai|
|**Platinimas internetu**|Negalima lengvai platinti internetu dėl didelio failo dydžio |Kompaktiškas failo dydis leidžia lengvai platinti internetu|
|**Suderinamumas**|Populiariausias muzikos ir garso klausymo kodekas, beveik suderinamas su kiekvienu planetos įrenginiu. Suderinamas su naujos kartos kompiuteriais, telefonais, AV imtuvais, Blu-ray grotuvais, srautinio perdavimo įrenginiais, tokiais kaip Roku arba Fire TV|

## Nuorodos Nr.

- [FLAC - Wikipedia](https://en.wikipedia.org/wiki/FLAC)

