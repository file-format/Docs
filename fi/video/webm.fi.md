---
date: 2019-10-11
keywords: WEBM, What is a WEBM file, WEBM File Format
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Lansaita WEBM-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata WEBM-tiedostons.
title: WEBM - WebM-videotiedostolomakeat
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Mikä on WEBM-tiedosto?

Tiedosto, jonka laajennus on .webm, on videotiedosto, joka perustuu avoimeen, rojaltivapaaseen WebM-tiedostomuotoon. Se on suunniteltu videon jakamiseen verkossa ja määrittää tiedostosäiliörakenteen, mukaan lukien video- ja äänimuodot. WebM on 100 % ilmainen, ja se toteuttaa korkealaatuisia avoimiin teknologioihin, kuten HTML:ään, HTTP:hen ja TCP/IP:hen, perustuvaa, jotka ovat avoimia kaikille käyttöönotettavaksi. WebM on erityisesti suunniteltu tarjoamaan videoita verkossa, mikä tekee siitä optimoidun suoratoistoon pienellä laskennallisella jalanjäljellä. Tämä tekee siitä sopivan videoiden toistamiseen kaikilla laitteilla, erityisesti pienitehoisilla netbookeilla, kämmentietokoneilla ja tableteilla.

## WEBM-tiedostomuoto

WebM-tiedostorakenne perustuu Matroska [MKV](/video/mkv/) -säiliötiedostomuodon osajoukkoon. WebM-tiedostossa saatavilla olevat videovirrat pakataan VP8- tai VP9-pakkaustekniikoilla, jotka ovat erittäin tehokkaita pakkaamisessa. Samoin WebM-tiedoston äänivirrat pakataan käyttämällä Vorbis- tai Opus-koodekkeja, jotka [Xiph Foundation](https://www.xiph.org/) on kehittänyt. Kaikki nämä videot ja äänikoodekit ovat rojaltivapaita ja niitä voidaan käyttää ilman maksuja.

Seuraavassa on yhteenveto WebM-tiedostomuodon teknisistä tiedoista.

|Kenttä|Kuvaus|
---|---|
|MIME-tyyppinen |video/webm|
|Vain ääni MIME-tyyppinen |ääni/webm|
|Uniform Type Identifier| org.webmproject.webm|
|Videon koodekin nimi| VP8 tai VP9|
|Äänikoodekin nimi| Vorbis tai Opus|

### WebM-elementit

WebM, being a subset of the Matroska specifications, provides support for some of the Matroska functionality. Following is a description of the supported elements.

#### EBML

|Nimi |Kuvaus|
---|---|
|EBML|Aseta seuraavien tietojen EBML-ominaisuudet. Jokaisen EBML-dokumentin on aloitettava tällä.|
|EBMLVersion |Tiedoston luomiseen käytetyn EBML-jäsentimen versio.|
|EBMLReadVersion|Minimi EBML-versio, jota jäsentimen on tuettava tämän tiedoston lukemiseen.|
|EBMLMaxIDLength |Tästä tiedostosta löytyvien tunnusten enimmäispituus (Matroskassa enintään 4).|
|EBMLMaxSizeLength|Tästä tiedostosta löytyvien kokojen enimmäispituus (8 tai vähemmän Matroskassa). Tämä ei ohita elementin alussa ilmoitettua elementtikokoa. Elementit, joiden ilmoitettu koko on suurempi kuin EBMLMaxSizeLength sallii, katsotaan kelpaamattomiksi.|
|DocType|Merkkijono, joka kuvaa tätä EBML-otsikkoa seuraavan asiakirjan tyyppiä (webm tässä tapauksessa).|
|DocTypeVersion|DocType-tulkin versio, jota käytettiin tiedoston luomiseen.|
|DocTypeReadVersion|Vähimmäis DocType-versio, jota tulkin on tuettava tämän tiedoston lukemiseen.|

#### Globaalit elementit

Tällä hetkellä tuetaan vain Void-elementtiä, jota käytetään mitätöimään vaurioituneet tiedot, jotta vältytään odottamattomilta käytöksiltä vaurioituneita tietoja käytettäessä. Sisältö hylätään. Käytetään myös varaamaan tilaa alielementissä myöhempää käyttöä varten.

#### Segmentti
Tämä elementti sisältää kaikki muut huipputason (tason 1) elementit. Tyypillisesti Matroska-tiedosto koostuu yhdestä segmentistä.

#### Meta Etsi tietoa

Seuraavia tiedonhakuja tuetaan.

|Elementin nimi |Kuvaus|
---|---|
|SeekHead |Sisältää toisen tason 1 elementin sijainnin.|
|Seek |Sisältää yhden hakumerkinnän EBML-elementtiin.|
|SeekID |Elementin nimeä vastaava binaaritunnus.|
|SeekPosition |Elementin sijainti segmentissä okteteina (0 = ensimmäinen tason 1 elementti).|

## Viitteet

* [WebM](https://www.webmproject.org/)

* [WebM-koodivarastot](https://www.webmproject.org/code/#webp-repositories)


