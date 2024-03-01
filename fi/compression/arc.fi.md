---
date: 2019-12-09
keywords: arc, .arc, arc file format, how to open arc files, .arc extension, arc extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARC-tiedostolomakeat
linktitle: ARC
description: Lansaitse ARC-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata ARC-tiedostons.
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Mikä on ARC-tiedosto?

ARC on System Enhancement Associatesin (SEA) kehittämä häviötön tietojen pakkaus- ja arkistointimuoto. Sekä tiedostomuotoa että sen luovaa sovellusta kutsutaan nimellä ARC. ARC oli erittäin suosittu puhelinverkkoyhteyden BBS:n alkuaikoina, koska se yhdisti pakkaamisen ja useiden tiedostojen arkistoinnin samaan tiedostoon. ARC korvattiin myöhemmin [ZIP](/compression/zip/):lla, joka tarjosi paremmat pakkaussuhteet.

.arc-tiedostotunnistetta käyttävät useat muut asiaankuulumattomat arkistotiedostotyypit, kuten Internet-arkiston käyttämä ARC-muoto useiden verkkoresurssien tallentamiseen, erilainen ARC-muoto, jota FreeArc-arkistaattori käyttää, eri muoto, jota Nintendo käyttää resursseihin jne. .

## ARC-tiedostomuodon lyhyt historia

The ARC program was written by Thom Henderson of System Enhancement Associates in 1985. Tämä ohjelma ryhmitti tiedostot yhdeksi arkistotiedostoksi ja myös pakkasi ne. ARC-ohjelman luomissa tiedostoissa käytettiin .arc-tunnistetta. SEA julkaisi ARC:n lähdekoodin vuonna 1986 ja Howard Chu siirsi ARC:n Unixille ja Atari ST:lle vuonna 1987.

Phil Katz kehitti PKARCin ja PKXARC:n tiedostojen arkistointiin ja purkamiseen. Tiedostot toimivat ARC-tiedostomuodossa ja olivat huomattavasti nopeampia. Toisin kuin ARC, Katz jakoi pakkaus- ja arkistointitoiminnot kahden eri tiedoston kesken, mikä vähensi muistin tarvetta niiden suorittamiseen.

SEA:n ja Katzin välisen oikeusjutun jälkeen SEA vetäytyi shareware-markkinoilta ja kehitti ARC+Plusin koko näytön käyttöliittymällä. ARC-muoto ei ole enää yleinen PC:llä.

## ARC-tiedostomuoto

ARC-tiedosto koostuu sekvenssistä tiedoston otsikoista ja tiedostoista, joita seuraa arkiston loppumerkki alla olevan kuvan mukaisesti.

```console
  file header 1
    file 1
  file header 2
    file 2
  .
  .
  file header n
    file n
EOF
```

### ARC-tiedoston otsikko ###

|Offset|Etiketti|Tyyppi|Arvo|Kuvaus|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|Menetelmä|
|02|ARCFNT|DS|12|tiedostonimi|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Pakattu koko|
|13|ARCDAT|DW|0000|Tiedostopäivämäärä (MSDOS)|
|15|ARCTIM|DW|0000|Tiedostoaika (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Pakkaamaton koko|
|1D|ARCFIL|DS|ARCNSZ| |

### Pakkausmenetelmät ###

Pakkausmenetelmätavu ilmaisee käytetyn pakkausmenetelmän. Seuraavat ovat ARC-tiedostossa käytetyt pakkausmenetelmät.

|Metod|Nimi|Kuvaus|
|---|---|---|
|0|Tallennettu|Ei pakkausta käytetty|
|1|Pakattu|Toistuva kulkupituuskoodaus (RLE)|
|2|Squeezed|Huffman-koodaus|
|3|Crunched|LZW 4K-puskurilla, 12-bittiset koodit|
|4|Crunched|Ensin pakkaus, sitten LZW 4K -puskuri 12 bitillä|
|5|Crunched|Pakkaus, LZW, 4K-puskuri, vaihteleva pituus (9-12 bittiä)|
|6|Squashed|LZW, 8K puskuri, vaihteleva pituus (9-13 bittiä)|
|7|Murskattu|Pakkaus, sitten LZW 8K -puskuri, 2-13 bittiä (PAK 1.0)|
|8|Distill|Dynamic Huffman 8K-puskurilla (PAK 2.0)|

## Viitteet

- {{HYPERLINKKI}})

