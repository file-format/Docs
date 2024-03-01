---
date: 2020-08-12
keywords: flif, .flif, flif file format, how to open flif files, .flif extension, flif extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: FLIF-tiedostolomakeat
linktitle: FLIF
description: Lansaita FLIF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata FLIF-tiedostons.
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Mikä on FLIF-tiedosto? ##

FLIF (Free Lossless Image Format) on häviötön kuvamuoto, joka käyttää tiedostoissaan .flif-laajennusta. FLIF väittää olevansa pakkaussuhteessa parempia kuin [PNG](/image/png/), häviöttömät [WebP](/image/webp/), häviötön BPG ja häviötön JPEG 2000. FLIF käyttää progressiivista lomitusta, jonka ansiosta mitä tahansa kuvan osittaista latausta voidaan käyttää häviöllisenä koodauksena koko kuvalle.

## Lyhyt historia ##

FLIF was announced in September 2015, and the alpha version was released in October 2015. Syyskuussa 2016 julkaistiin ensimmäinen vakaa versio FLIF:stä.

## FLIF Design ##

FLIF käyttää muunnelmaa CABAC:sta (Context-adaptive binary aritmetic coding) ja MANIACista (Meta-Adaptive Near-zero Integer Aithmetic Coding) pakkaamiseen. MANIAC on Jon Sneyersin ja Pieter Wuillen kehittämä entropiakoodausalgoritmi. MANIACissa kontekstit ovat päätöspuiden solmuja, jotka opitaan koodaushetkellä dynaamisesti. Tämä tekee kontekstimallista kuvakohtaisemman ja parantaa pakkausta. FLIF:llä on seuraavat ominaisuudet:

- Tukee häviötöntä pakkausta
- Tukee häviöllistä pakkausta kooderin esikäsittelyllä
- Tukee harmaasävy-, RGB- ja RGBA-sävyjä
- Tukee värisyvyyttä 1-16 bittiä kanavaa kohti
- Tukee lomitettuja ja ei-lomitettuja tiedostoja
- Tukee osittain ladattujen tiedostojen progressiivista dekoodausta
- Tukee animaatioita
- Tukee upotettuja ICC-väriprofiileja, Exif- ja XMP-metatietoja
- Rajallinen tuki kameran raakatiedostojen pakkaamiselle (RGGB)

## FLIF-tiedostomuoto ##

FLIF-tiedostossa on seuraavat neljä osaa:

## Pääotsikko ##

Pääotsikko sisältää tärkeimmät metatiedot, mukaan lukien leveys, korkeus, värisyvyys ja kehysten lukumäärä.

|Tyyppi|Arvo|Kuvaus|
|---|---|---|
|4 tavua|FLIF|Magic|
|4 bittiä|3 = ni still; 4 = olen edelleen; 5 = ni anim; 6 = i anim|Lomitus, animaatio|
|4 bittiä|1 = harmaasävy; 3 = RGB; 4 = RGBA|Kanavien määrä (nb_channels)|
|1 tavu|'0','1','2' ('0'=mukautettu)|Tavua kanavaa kohti (Bpc)|
|varint|leveys-1|Leveys|
|varint|korkeus-1|Korkeus|
|varint|nb_frames-2 (vain jos animaatio)|Kuvien määrä (nb_frames)|

## Metatietopalat ##

Tämä osa sisältää ei-pikseleitä, kuten Exif/XMP-metatietoja, ICC-väriprofiilia jne., jotka on koodattu DEFLATE-pakkauksella. Nämä palat määritellään samalla tavalla kuin PNG-palat sillä erolla, että istukan koko on koodattu vaihtelevalla tavumäärällä. Osien nimet voivat olla 4 kirjainta (4 tavua) pitkiä tai alle 32:ta, mikä tarkoittaa ei-valinnaista kappaletta.

Seuraavassa on esimerkki valinnaisista istukkaista:

|Osan nimi|Kuvaus|Sisältö (DEFLATE-dekompression jälkeen)|
|---|---|---|
|iCCP|ICC-väriprofiili|raaka ICC-väriprofiilitiedot|
|eXif|Exif-metadata|Exif\0\0-otsikko, jota seuraa TIFF-otsikko ja EXIF-tiedot|
|eXmp|XMP-metatiedot|XMP sisältyy vain luku -muotoiseen xpacket-pakettiin ilman täyttöä|

### Nimeämissopimus ###

- **Ensimmäinen kirjain**: Isoja kirjaimia käytetään kriittisille ja pienille ei-kriittisille paloille.
- **Toinen kirjain**: Isoja kirjaimia käytetään julkisissa kirjaimissa ja pieniä yksityisiä paloja
- **Kolmas kirjain**: Isoja kirjaimia käytetään istukkaille, joita tarvitaan kuvan näyttämiseen oikein, ja pienet kirjaimet eivät ole tärkeitä kuvan näyttämiseksi.
- **Neljäs kirjain**: Isoja kirjaimia käytetään istukkaille, jotka voidaan kopioida turvallisesti sokeasti. Pienet kirjaimet riippuvat kuvatiedoista.

## Toinen otsikko ##

Tämä sisältää tiedot pikselien todellisesta koodauksesta.

|Tyyppi|Kuvaus|Kunto|Oletusarvo|
|---|---|---|---|
|1 tavu|NUL-tavu (0x00), FLIF16-bittivirran osanimi||
|uni_int(1,16)|Bittiä pikseliä kohden kanavia|Bpc == '0': toista(nb_channels)|8 jos Bpc == '1', 16 jos Bpc == '2'|
|uni_int(0,1)|Lippu: alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|silmukoiden määrä|nb_frames > 1||
|uni_int(0,60_000)|Kehysviive ms|nb_frames > 1: toista(nb_frames)|
|uni_int(0,1)|Lippu: has_custom_cutoff_and_alpha|||
|uni_int(1,128)|cutoff|on_custom_cutoff_and_alpha|2|
|uni_int(2,128)|alfajakaja|on_mukautettu_leikkaus_ja_alpha|19|
|uni_int(0,1)|Lippu: has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|on_custom_bitchance||
|muuttuja|Transformaatiot (katso alla)|||
|uni_int(1) = 0|Osoitinbitti: tehty muunnoksilla|||
|uni_int(0,2)|Näkymätön pikselin ennustaja|alfa_nolla && lomitettu && alfa-alue sisältää nollan||

**kanavat**

|Kanavan numero|Kuvaus|
|---|----|
|0|Punainen tai harmaa|
|1|Vihreä|
|2|Sininen|
|3|Alfa|

**Muunnat**

|Tyyppi|Kuvaus|
|---|---|
|uni_int(1) = 1|Osoitinbitti: ei vielä tehty|
|uni_int(0,13)|Transformaatiotunniste|
|muuttuja|Muunnostiedot (riippuu muunnoksesta)|

Transformaatiota käytetään pikselitietojen muokkaamiseen paremman pakkauksen saamiseksi ja todellisten esiintyvien pikseliarvojen seuraamiseen.

## Pikselitiedot ##

Tämä osa sisältää todellisen pikselidatan, joka on koodattu MANIAC-entropiakoodauksella. Pikselit voidaan koodata käyttämällä lomitettua tai lomittamatonta koodausta.

### Lomitettu menetelmä ###

In this method, zoomlevels are defined. Zoomlevel 0 is used for the full image, zoomlevel 1 is used for all even-numbered rows, zoomlevel 2 is used for all even-numbered columns of zoomlevel 1. Toisin sanoen jokainen parillinen zoomaustaso 2k on kuvan alasnäytteinen versio mittakaavassa 1:2^k. Zoomaustasot on koodattu korkeimmasta alimpaan.

### Lomitettu menetelmä ###

Tässä menetelmässä MANIAC-puiden koodaus alkaa välittömästi, mitä seuraa pikselien koodaus.

## Viitteet ##

- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

