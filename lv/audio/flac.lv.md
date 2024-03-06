---
date: 2019-12-13
keywords: flac, flac file format, .flac extension, flac file, flac vs mp3
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lnopelniet par FLAC faila formātu un API, kas var izveidot un atvērt FLAC failus.
title: FLAC faila veidlapaat
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## Kas ir FLAC fails?

FLAC (Free Lossless Audio Codec) ir bezzudumu kompresijas audio kodēšanas formāts, ko izstrādājis Xiph.Org Foundation. FLAC ir bezatlīdzības atvērts formāts, kas tiek saglabāts ar paplašinājumu .flac. Digitālais audio, kas saspiests, izmantojot FLAC algoritmu, parasti tiek samazināts līdz 50–70 procentiem. FLAC failus var atspiest, veidojot identisku oriģinālo audio failu kopiju.

## FLAC faila formāts

Šis ir FLAC bitu plūsmas pārskats.

- **fLaC marķieris**: šis marķieris tiek pievienots straumes sākumam. Tam seko viens vai vairāki metadatu bloki.
- **Metadatu bloki**: FLAC atbalsta 128 veidu metadatu blokus; pašlaik ir definēti šādi.
  - "**STREAMINFO**: satur informāciju par visu straumi."
  - "**LIETOJUMS**: to izmanto trešo pušu lietojumprogrammas identifikācijai."
  - "**PADDING**: tiek izmantots, lai rezervētu vietu metadatiem, ja metadati tiks rediģēti pēc kodēšanas. Kad metadati tiek rediģēti, pildījums tiek aizstāts ar faktiskajiem metadatiem."
  - "**SEEKTABLE**: izvēles tabula meklēšanas punktu glabāšanai."
  - "**VORBIS_COMMENT**: izmanto, lai saglabātu cilvēkam lasāmus atslēgu/vērtību pārus."
  - "**CUESHEET**: izmanto, lai saglabātu informāciju par norāžu lapu."
  - "**PICTURE**: izmanto attēlu saglabāšanai."
- **FRAME**: audio dati sastāv no viena vai vairākiem audio kadriem.
  - "**FRAME_HEADER**: satur pamatinformāciju par straumi."
  - "**APAKŠKADS**: lai samazinātu sarežģītību, atsevišķi apakškadri tiek kodēti atsevišķi kadrā (viens kadrs katrā kanālā)."
  - "**FRAME_FOOTER**: satur visa kadra CRC."

## Īsa FLAC faila formāta vēsture

Josh Coalson began the development of FLAC in 2000. Pirmā FLAC versija tika izlaista 2001. gada 20. jūlijā. FLAC tika iekļauts Xiph.Org karogā 2003. gada 20. janvārī. FLAC izstrāde tika pārvietota uz Xiph.Org git repozitoriju, 26. martā izlaižot versiju 1.3.0. 2013. gads.

## FLAC projekta sastāvs

FLAC projekts sastāv no šādiem elementiem:

- Straumēšanas formāti.
- Vienkāršs straumes konteinera formāts (FLAC).
- libFLAC: atsauces kodētāju, dekodētāju un metadatu saskarnes bibliotēka.
- libFLAC++: objektorientēts libFLAC iesaiņojums.
- flac: komandrindas programma FLAC straumju kodēšanai un atkodēšanai.
- metaflac: komandrindas metadatu redaktors FLAC.
- Ievades spraudņi mūzikas atskaņotājiem, piemēram, Winamp, XMMX utt.
- Ogg konteinera formāts (Ogg FLAC).

## FLAC dizains

Atkarībā no mūzikas blīvuma un amplitūdas saspiestā faila izmērs var būt par 80% mazāks nekā oriģinālā faila izmērs.

### Avota kodētājs ###

- Tas atbalsta tikai veselu skaitļu paraugus, nevis peldošā komata paraugus. Tas var apstrādāt PCM bitu izšķirtspēju no 4 līdz 32 bitiem uz vienu paraugu un paraugu ņemšanas frekvenci no 1 Hz līdz 65 535 Hz. FLAC kodējums ir ierobežots līdz 24 bitiem vienā paraugā.
- Kanālus var grupēt, lai izmantotu starpkanālu korelācijas un palielinātu saspiešanu.
- CRC kontrolsummas tiek izmantotas, lai identificētu bojātus kadrus.
- Audio paraugu konvertēšanai FLAC izmanto lineāro prognozēšanu.

### Metadati ###

- FLAC atbalsta ReplayGain (izmanto, lai uztvertu un normalizētu audio skaļumu).
- FLAC atzīmēšanai izmanto to pašu sistēmu, ko izmanto Vorbis komentāros.
- libFLAC izmanto lielākā daļa FLAC lietojumprogrammu kodēšanai/dekodēšanai.
- libFLAC API ir sakārtots straumēs, meklējamās straumēs un failos, lai palielinātu abstrakciju no bāzes FLAC bitu straumes.

### Saspiešana ###

libFLAC izmanto saspiešanas līmeņus no 0 līdz 8, kur 0 ir ātrākais un 8 ir lēnākais saspiešanas līmenis. Saspiestie faili vienmēr ir bez zudumiem, lai gan kompromiss ir starp ātrumu un lielumu.

## FLAC pret MP3
MP3 ir saspiešanas formāts ar zaudējumiem, kas nozīmē, ka pēc saspiešanas tas var samazināt daļu audio, lai samazinātu tā lielumu. Tā kā FLAC ir bezzudumu faila formāts, kas nozīmē, ka jūs varat dzirdēt audio tā tīrākajā formā. Agrāk bezzudumu failu formāti bija CDA vai WAV, kas nebija tik daudz vietas efektīvi kā FLAC. Šajā tabulā ir parādīts šo divu formātu salīdzinājums dažiem svarīgiem terminiem.

|Termiņš|FLAC|MP3|
---|---|---|
|**Datu kvalitāte**|Nav nekādu audio datu zudumu| Saspiežot audio datus, var tikt zaudēti daži dati|
|**Izmērs**|Lielāks faila izmērs, salīdzinot ar formātiem ar zudumiem. Tāpēc nepieciešama lielāka uzglabāšanas jauda| Mazāks faila izmērs, piemērots atskaņošanai kompaktās audio ierīcēs ar nelielu atmiņas vietu |
|**Aparatūras prasības**| Nepieciešams augstas kvalitātes audio aprīkojums un milzīga atmiņas ietilpība | Mazākā krātuves vietā var saglabāt milzīgas audio bibliotēkas. Piemērots rokas ierīcēm, piemēram, audio atskaņotājiem vai mobilajiem tālruņiem|
|**Izplatīšana internetā**|Nevar viegli izplatīt internetā, jo ir liels faila lielums |Kompakts faila izmērs atvieglo izplatīšanu internetā|
|**Saderība**|Populārākais mūzikas un audio klausīšanās kodeks, kas gandrīz saderīgs ar visām ierīcēm uz planētas. Saderīgs ar jaunās paaudzes datoriem, tālruņiem, AV uztvērējiem, Blu-ray atskaņotājiem, straumēšanas ierīcēm, piemēram, Roku vai Fire TV|

## Atsauces Nr.

- [FLAC - Wikipedia](https://en.wikipedia.org/wiki/FLAC)

