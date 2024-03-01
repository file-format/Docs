---
date: 2019-12-13
keywords: flac, flac file format, .flac extension, flac file, flac vs mp3
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lansaita FLAC-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata FLAC-tiedostons.
title: FLAC-tiedostolomakeat
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## Mikä on FLAC-tiedosto?

FLAC (Free Lossless Audio Codec) on Xiph.Org Foundationin kehittämä häviötön pakkausäänen koodausmuoto. FLAC on rojaltivapaa avoin muoto, joka tallennetaan .flac-tunnisteella. FLAC-algoritmilla pakatun digitaalisen äänen koko pienennetään tyypillisesti 50–70 prosenttiin. FLAC-tiedostot voidaan purkaa alkuperäisten äänitiedostojen identtisiksi kopioiksi.

## FLAC-tiedostomuoto

Tämä on yleiskatsaus FLAC-bittivirrasta.

- **fLaC-merkki**: Tämä merkki lisätään streamin alkuun. Sitä seuraa yksi tai useampi metatietolohko.
- **Metatietolohkot**: FLAC tukee 128 erilaista metatietolohkoa; tällä hetkellä määritellään seuraavat.
  - "**STREAMINFO**: Sisältää tiedot koko streamista."
  - "**SOVELLUS**: Tätä käyttävät kolmannen osapuolen sovellukset tunnistamiseen."
  - "**TÄYTE**: Sitä käytetään varaamaan tilaa metatiedoille, jos metatietoja muokataan koodauksen jälkeen. Kun metatietoja muokataan, täyte korvataan todellisella metatiedolla."
  - "**HAKUTAULUKKO**: Valinnainen taulukko hakupisteiden tallentamiseen."
  - "**VORBIS_COMMENT**: Käytetään ihmisen luettavien avain/arvo-parien tallentamiseen."
  - "**CUESHEET**: Käytetään vihjearkin tietojen tallentamiseen."
  - "**PICTURE**: Käytetään kuvien tallentamiseen."
- **FRAME**: Audiodata koostuu yhdestä tai useammasta äänikehyksestä.
  - "**FRAME_HEADER**: Sisältää perustiedot streamista."
  - "**ALIKEHYS**: Monimutkaisuuden vähentämiseksi yksittäiset alikehykset koodataan erikseen kehyksen sisällä (yksi kehys kanavaa kohti)."
  - "**FRAME_FOOTER**: Sisältää koko kehyksen CRC:n."

## FLAC-tiedostomuodon lyhyt historia

Josh Coalson began the development of FLAC in 2000. Ensimmäinen FLAC-versio julkaistiin 20. heinäkuuta 2001. FLAC liitettiin Xiph.Org-lipun alle 20. tammikuuta 2003. FLAC:n kehitys siirrettiin Xiph.Orgin git-arkistoon, kun versio 1.3.0 julkaistiin 26. maaliskuuta 2013.

## FLAC-projektin kokoonpano

FLAC-projekti koostuu seuraavista:

- Suoratoistomuodot.
- Yksinkertainen säilömuoto streamille (FLAC).
- libFLAC: Viitekooderien, dekooderien ja metatietoliittymän kirjasto.
- libFLAC++: libFLACin oliopohjainen kääre.
- flac: komentoriviohjelma FLAC-virtojen koodaamiseen ja purkamiseen.
- metaflac: komentorivin metatietoeditori FLAC:lle.
- Syöttölaajennukset musiikkisoittimille, kuten Winamp, XMMX jne.
- Ogg-säiliömuoto (Ogg FLAC).

## FLAC-suunnittelu

Musiikin tiheydestä ja amplitudista riippuen pakatun tiedoston koko voi olla 80 % pienempi kuin alkuperäinen tiedosto.

### Lähdekooderi ###

- Se tukee vain kokonaislukunäytteitä, ei liukulukua. Se pystyy käsittelemään PCM-bitin resoluutiota 4 - 32 bittiä näytettä kohti ja näytteenottotaajuutta 1 Hz - 65 535 Hz. FLAC-koodaus on rajoitettu 24 bittiin näytettä kohti.
- Kanavat voidaan ryhmitellä hyödyntääksesi kanavien välisiä korrelaatioita pakkaamisen lisäämiseksi.
- CRC-tarkistussummia käytetään vioittuneiden kehysten tunnistamiseen.
- Ääninäytteiden muuntamiseen FLAC käyttää lineaarista ennustetta.

### Metatiedot ###

- FLAC tukee ReplayGainia (käytetään havaitsemaan ja normalisoimaan äänen voimakkuutta).
- FLAC käyttää samaa järjestelmää, jota käytetään Vorbis-kommenteissa taggaukseen.
- Useimmat FLAC-sovellukset käyttävät libFLACia koodaukseen/dekoodaukseen.
- libFLAC API on järjestetty virroiksi, haettaviksi virroiksi ja tiedostoiksi, jotta voidaan lisätä abstraktiota FLAC-perusbittivirrasta.

### Puristus ###

libFLAC käyttää pakkaustasoja 0-8, jossa 0 on nopein ja 8 on hitain pakkaustaso. Pakatut tiedostot ovat aina häviöttömiä, vaikka kompromissi on nopeuden ja koon välillä.

## FLAC vs MP3
MP3 on häviöllinen pakkausmuoto, mikä tarkoittaa, että se voi leikata osan äänestä pienentääkseen sen kokoa pakkaamisen jälkeen. FLAC on häviötön tiedostomuoto, mikä tarkoittaa, että voit kuulla äänen puhtaimmassa muodossaan. Aiemmin häviöttömät tiedostomuodot olivat CDA tai WAV, jotka eivät olleet paljon tilaa säästäviä kuin FLAC. Seuraava taulukko näyttää näiden kahden muodon vertailun joidenkin tärkeiden termien osalta:

|Termin|FLAC|MP3|
---|---|---|
|**Tiedonlaatu**|Ei äänidatan menetystä| Osa tiedoista voi kadota äänidataa pakatessa|
|**Koko**|Suurempi tiedostokoko verrattuna häviöllisiin muotoihin. Tarvitaan siis suurempi tallennuskapasiteetti| Pienempi tiedostokoko, sopii toistamiseen pienikokoisilla äänilaitteilla, joissa on vähän tallennustilaa |
|**Laitteistovaatimukset**| Tarvitset korkealaatuisia äänilaitteita ja valtavan tallennuskapasiteetin | Valtavia äänikirjastoja voidaan tallentaa pienempään tallennustilaan. Sopii kämmenlaitteille, kuten soittimille tai matkapuhelimille|
|**Jakelu Internetin kautta**|Ei voida levittää helposti Internetin kautta massiivisen tiedostokoon vuoksi |Koko tiedostokoko helpottaa jakamista Internetissä|
|**Yhteensopivuus**|Suosituin musiikin ja äänen kuuntelukoodekki, joka on lähes yhteensopiva kaikkien planeetan laitteiden kanssa. Yhteensopiva uuden sukupolven tietokoneiden, puhelimien, AV-vastaanottimien, blu-ray-soittimien, suoratoistolaitteiden, kuten Roku tai Fire TV|

## Viitteet ##

- {{HYPERLINKKI1}}

