---
date: 2020-08-12
keywords: jxr, .jxr, jxr file format, how to open jxr files, .jxr extension, jxr extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JXR-tiedostolomakeat
linktitle: JXR
description: Lansaitse JXR-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata JXR-tiedostons.
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## Mikä on JXR-tiedosto? ##

JPEG XR (JPEG Extended Range) on jatkuvasävyisten valokuvakuvien tiedostomuoto. Se on still-kuvien pakkausstandardi, joka perustuu Microsoftin kehittämään HD Photo -kuvaan. Se tukee sekä häviöllistä että häviötöntä pakkausta.

## Lyhyt historia ##

Windows Media Photo was first announced by Microsoft at WinHEC 2006. Se nimettiin uudelleen HD Photo -kuvaksi marraskuussa 2006. JPEG XR hyväksyttiin kansainväliseksi standardiksi ISO/IEC 29199-2 19. kesäkuuta 2009. ITU-T ja ISO/IEC julkaisivat liikeformaatin määrittelyn (ITU-T T.833 | ISO/ IEC 29199-3), vaatimustenmukaisuustestisarja (ITU-T T.834 | ISO/IEC 29199-4) ja viiteohjelmisto (ITU-T T.835 | ISO/IEC 29199-5) JPEG XR:lle valmistumisen jälkeen kuvan koodausspesifikaatiosta vuonna 2010. Vuonna 2011 julkaistiin tekninen raportti, joka kuvaa JPEG XR:n työnkulkuarkkitehtuuria.

## JPEG XR Design ##

JPEG:iin verrattuna JPEG XR tarjoaa useita parannuksia, mukaan lukien:

- **Parempi pakkaus**: JPEG XR tarjoaa korkeammat pakkaussuhteet.
- **häviötön pakkaus**: JPEG XR tukee häviötöntä pakkausta.
- **Tile Structure**: JPEG XR -kuva voidaan segmentoida ruutualueisiin, joissa jokainen alue voidaan purkaa erikseen.
- **Lisää väritarkkuutta**: JPEG XR sisältää sisäisen muunnoksen YCoCg-väriavaruuteen kuvien tukemiseksi RGB-väriavaruuden avulla. JPEG XR tukee myös 16-bittistä komponenttia kohti (64-bittinen pikseliä kohti) CMYK-kokonaislukumallia. JPEG XR tukee RGBE-jaetun eksponentin liukulukuvärimuotoa HDR-kuville. JPEG XR tukee myös harmaasävy- ja monikanavaisia värikoodauksia.
- **Läpinäkyvyyskartta**: JPEG XR tukee alfakanavaa läpinäkyvyyden takaamiseksi.
- **Pakatun verkkotunnuksen kuvan muokkaus**: JPEG XR -kuvat voidaan muuntaa häviölliseen koodaukseen, resoluutiota pienentää, rajata, kääntää, kiertää ja ruudun rakennetta voidaan muuttaa ilman tiedoston täydellistä dekoodausta.
- **Metatietojen tuki**: JPEG XR -kuvatiedosto voi sisältää ICC-väriprofiilin, joka takaa yhtenäisen väriesityksen useissa laitteissa. Muoto tukee myös Exif- ja XMP-metatietomuotoja.

## Säilön muoto ##

JPEG XR -kuvatiedot voidaan tallentaa TIFF-tyyppisessä säilömuodossa käyttämällä IFT (Image File Directory) -tunnisteiden taulukkoa. JXR-tiedosto sisältää seuraavat IFD-tunnisteet:

- Kuvatiedot: Se on jatkuva itsenäinen kuvadata.
- Valinnainen alfakanavan data: Jos tämä on olemassa, kuvatiedot voidaan pakata erikseen mahdollistaen sellaisten sovellusten tukemisen, jotka eivät tue läpinäkyvyyttä.
- Metadata
- Valinnaiset XMP-metatiedot
- Valinnaiset Exif-metatiedot

Koska se perustuu TIFF-muotoon, se perii kaikki TIFF-muodon rajoitukset, kuten 4 Gt:n tiedostokokorajoituksen.

## Viitteet ##

- {{HYPERLINKKI1}}

