---
date: 2020-08-12
keywords: flif, .flif, flif file format, how to open flif files, .flif extension, flif extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: FLIF faila veidlapaat
linktitle: FLIF
description: Lnopelniet par FLIF faila formātu un API, kas var izveidot un atvērt FLIF failus.
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Kas ir FLIF fails? ##

FLIF (Free Lossless Image Format) ir bezzudumu attēla formāts, kura failiem tiek izmantots paplašinājums .flif. FLIF apgalvo, ka kompresijas pakāpes ziņā pārspēj [PNG](/image/png/), bezzudumu [WebP](/image/webp/), bezzudumu BPG un bezzudumu JPEG 2000. FLIF izmanto progresīvo pīšanos, kuras dēļ jebkura attēla daļēja lejupielāde var tikt izmantota kā visa attēla zudumu kodējums.

## Īsa vēsture ##

FLIF was announced in September 2015, and the alpha version was released in October 2015. 2016. gada septembrī tika izlaista pirmā stabilā FLIF versija.

## FLIF dizains ##

FLIF saspiešanai izmanto CABAC (kontekstam adaptīvā binārā aritmētiskā kodēšana), MANIAC (metaadaptīvā gandrīz nulles veselo skaitļu aritmētiskā kodēšana) variantu. MANIAC ir entropijas kodēšanas algoritms, ko izstrādājuši Jon Sneyers un Pieter Wuille. Programmā MANIAC konteksti ir lēmumu koku mezgli, kas tiek apgūti kodēšanas laikā dinamiski. Tas padara konteksta modeli raksturīgāku attēlam un nodrošina labāku saspiešanu. FLIF ir šādas funkcijas:

- Atbalsta bezzudumu saspiešanu
- Atbalsta zudumu saspiešanu ar kodētāja priekšapstrādi
- Atbalsta pelēktoņu, RGB un RGBA
- Atbalsta krāsu dziļumu no 1 līdz 16 bitiem katrā kanālā
- Atbalsta pītās un bezpārlaides failus
- Atbalsta daļēji lejupielādēto failu pakāpenisku dekodēšanu
- Atbalsta animācijas
- Atbalsta iegultos ICC krāsu profilus, Exif un XMP metadatus
- Ir ierobežots atbalsts kameras neapstrādātu failu saspiešanai (RGGB)

## FLIF faila formāts ##

FLIF failam ir šādas četras daļas:

## Galvenā galvene ##

Galvenajā galvenē ir galvenie metadati, tostarp platums, augstums, krāsu dziļums, kadru skaits.

|Tips|Vērtība|Apraksts|
|---|---|---|
|4 baiti|FLIF|Maģija|
|4 biti|3 = ni joprojām; 4 = es joprojām; 5 = ni anim; 6 = i anim|Interlacing, animation|
|4 biti|1 = pelēktoņu; 3 = RGB; 4 = RGBA|Kanālu skaits (nb_channels)|
|1 baits|'0','1','2' ('0'=pielāgots)|Baiti kanālā (Bpc)|
|varint|platums-1|Platums|
|varint|augstums-1|Augums|
|varint|nb_frames-2 (tikai, ja animācija)|Kadru skaits (nb_frames)|

## Metadatu gabali ##

Šī daļa satur nepikseļus, piemēram, Exif/XMP metadatus, ICC krāsu profilu utt., kas ir kodēti, izmantojot DEFLATE kompresiju. Šie gabali ir definēti līdzīgi kā PNG gabali ar atšķirību, ka patronas lielums ir kodēts ar mainīgu baitu skaitu. Daļu nosaukumos var būt 4 burti (4 baiti) vai vērtība, kas ir mazāka par 32, kas norāda uz neobligātu gabalu.

Tālāk ir sniegts papildu patronu piemērs.

|Daļas nosaukums|Apraksts|Saturs (pēc DEFLATE-dekompresijas)|
|---|---|---|
|iCCP|ICC krāsu profils|neapstrādāti ICC krāsu profila dati|
|eXif|Exif metadata|Galvene Exif\0\0, kam seko TIFF galvene un EXIF dati|
|eXmp|XMP metadati|XMP ietverts tikai lasāmā xpacket bez polsterējuma|

### Nosaukšanas konvencija ###

- **Pirmais burts**: lielie burti tiek izmantoti kritiskiem burtiem, bet mazie burti tiek izmantoti nekritiskiem gabaliem.
- **Otrais burts**: lielie burti tiek izmantoti publiskajiem burtiem, bet mazie tiek izmantoti privātiem gabaliem
- **Trešais burts**: lielie burti tiek izmantoti, lai pareizi parādītu attēlu, un mazie burti nav svarīgi attēla parādīšanai.
- **Ceturtais burts**: Lielie burti tiek izmantoti patronām, kuras var droši kopēt akli. Mazo burtu patronas ir atkarīgas no attēla datiem.

## Otrā galvene ##

Tas satur informāciju par faktisko pikseļu kodējumu.

|Tips|Apraksts|Stāvoklis|Noklusējuma vērtība|
|---|---|---|---|
|1 baits|NUL baits (0x00), FLIF16 bitu straumes gabala nosaukums||
|uni_int(1,16)|Biti uz kanālu pikseļu|Bpc == '0': atkārtojiet(nb_channels)|8, ja Bpc == '1', 16, ja Bpc == '2'|
|uni_int(0,1)|Atzīmēts: alfa_nulle|nb_channels > 3|0|
|uni_int(0,100)|Cilpu skaits|nb_kadri > 1||
|uni_int(0,60_000)|Kadra aizkave ms|nb_frames > 1: atkārtojiet(nb_frames)|
|uni_int(0,1)|Karogs: has_custom_cutoff_and_alpha|||
|uni_int(1,128)|cutoff|ir_custom_cutoff_and_alpha|2|
|uni_int(2,128)|alfa dalītājs|ir_pielāgots_cutoff_and_alpha|19|
|uni_int(0,1)|Atzīmēts: has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|ir_custom_bitchance||
|mainīgais|Transformācijas (skat. zemāk)|||
|uni_int(1) = 0|Indikatora bits: veikts ar transformācijām|||
|uni_int(0,2)|Neredzams pikseļu prognozētājs|alfa_nulle && pārripots && alfa diapazons ietver nulli||

**Kanāli**

|Kanāla numurs|Apraksts|
|---|----|
|0|Sarkans vai Pelēks|
|1|Zaļš|
|2|Zils|
|3|Alfa|

**Pārvērtības**

|Tips|Apraksts|
|---|---|
|uni_int(1) = 1|Indikatora bits: vēl nav izdarīts|
|uni_int(0,13)|Transformācijas identifikators|
|mainīgais|Transformācijas dati (atkarīgs no transformācijas)|

Transformāciju izmanto, lai modificētu pikseļu datus labākai saspiešanai un sekotu faktiskajām pikseļu vērtībām.

## Pikseļu dati ##

Šī daļa satur faktiskos pikseļu datus, kas kodēti, izmantojot MANIAC entropijas kodēšanu. Pikseļus var kodēt, izmantojot rindpārleces vai bezpārlaides kodējumu.

### Interlaced metode ###

In this method, zoomlevels are defined. Zoomlevel 0 is used for the full image, zoomlevel 1 is used for all even-numbered rows, zoomlevel 2 is used for all even-numbered columns of zoomlevel 1. Citiem vārdiem sakot, katrs pāra skaitļa tālummaiņas līmenis 2k ir samazināta attēla versija mērogā 1:2^k. Tālummaiņas līmeņi ir kodēti no augstākā līdz zemākajam.

### Metode bez pīšanas ###

Izmantojot šo metodi, MANIAC koku kodēšana sākas uzreiz, kam seko pikseļu kodēšana.

## Atsauces Nr.

- [FLIF - Wikipedia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

